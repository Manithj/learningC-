## <u>mutable keyword</u>

The "mutable" keyword is a C++ keyword that can be used to modify the behavior of a non-const variable that is a member of a const object or reference.

In C++, when an object is declared as const, it means that its state cannot be modified. However, if the object contains a non-const member variable, that variable can still be modified, which can potentially lead to unexpected behavior.

The "mutable" keyword can be used to mark a member variable as mutable, which means it can be modified even if the object itself is declared as const. This allows for more fine-grained control over which parts of the object can be modified, while still enforcing const correctness in other parts of the code.

eg:-
```c++
#include <bits/stdc++.h>
#include <string.h>
using namespace std;

// Customer Class
class Customer {
	
	// class Variables
	string name;
	mutable string placedorder;
	int tableno;
	mutable int bill;

	// member methods
public:

	
	// constructor
	Customer(string s, string m, int a, int p)
	{
	name= s;
	placedorder=m;
	tableno = a;
	bill = p;
	}

	// to change the place holder
	void changePlacedOrder(string p) const
	{
	placedorder=p;
	}

	// change the bill
	void changeBill(int s) const { bill = s; }

	// to display
	void display() const
	{
	cout << "Customer name is: " << name << endl;
	cout << "Food ordered by customer is: "
		<< placedorder << endl;
	cout << "table no is: " << tableno << endl;
	cout << "Total payable amount: " << bill << endl;
	}
};

// Driver code
int main()
{
	const Customer c1("Pravasi Meet", "Ice Cream", 3, 100);
	c1.display();
	c1.changePlacedOrder("GulabJammuns");
	c1.changeBill(150);
	c1.display();
	return 0;
}
```

Output

```
Customer name is: Pravasi Meet
Food ordered by customer is: Ice Cream
table no is: 3
Total payable amount: 100
Customer name is: Pravasi Meet
Food ordered by customer is: GulabJammuns
table no is: 3
Total payable amount: 150
```
