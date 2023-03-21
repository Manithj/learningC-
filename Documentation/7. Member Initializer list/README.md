## <u>Member Initializer list</u>

Initializer List is used in initializing the data members of a class. The list of members to be initialized is indicated with constructor as a comma-separated list followed by a colon. Following is an example that uses the initializer list to initialize x and y of Point class.

```c++
#include<iostream>
using namespace std;

class Point {
private:
	int x;
	int y;
public:
	Point(int i = 0, int j = 0):x(i), y(j) {}
	/* The above use of Initializer list is optional as the
		constructor can also be written as:
		Point(int i = 0, int j = 0) {
			x = i;
			y = j;
		}
	*/
	
	int getX() const {return x;}
	int getY() const {return y;}
};

int main() {
Point t1(10, 15);
cout<<"x = "<<t1.getX()<<", ";
cout<<"y = "<<t1.getY();
return 0;
}
```

Output

```
x = 10
y = 15
```

## Use cases

### 1) For initialization of non-static const data members

- const data members must be initialized using Initializer List. In the following example, “t” is a const data member of Test class and is initialized using Initializer List. 
- Reason for initializing the const data member in the initializer list is because no memory is allocated separately for const data member, it is folded in the symbol table due to which we need to initialize it in the initializer list. 
- Also, it is a Parameterized constructor and we don’t need to call the assignment operator which means we are avoiding one extra operation. 

```c++
#include<iostream>
using namespace std;

class Test {
	const int t;
public:
	Test(int t):t(t) {} //Initializer list must be used
	int getT() { return t; }
};

int main() {
	Test t1(10);
	cout<<t1.getT();
	return 0;
}
```

Output

```
10
```

### 2) For initialization of reference members

Reference members must be initialized using Initializer List. In the following example, “t” is a reference member of Test class and is initialized using Initializer List.

```c++
// Initialization of reference data members
#include<iostream>
using namespace std;

class Test {
	int &t;
public:
	Test(int &t):t(t) {} //Initializer list must be used
	int getT() { return t; }
};

int main() {
	int x = 20;
	Test t1(x);
	cout<<t1.getT()<<endl;
	x = 30;
	cout<<t1.getT()<<endl;
	return 0;
}
```

Output

```
20
30
```

### 3) For initialization of member objects which do not have default constructor

In the following example, an object “a” of class “A” is data member of class “B”, and “A” doesn’t have default constructor. Initializer List must be used to initialize “a”.

```c++
#include <iostream>
using namespace std;

class A {
	int i;
public:
	A(int );
};

A::A(int arg) {
	i = arg;
	cout << "A's Constructor called: Value of i: " << i << endl;
}

// Class B contains object of A
class B {
	A a;
public:
	B(int );
};

B::B(int x):a(x) { //Initializer list must be used
	cout << "B's Constructor called";
}

int main() {
	B obj(10);
	return 0;
}
```

Output

```
A's Constructor called: Value of i: 10
B's Constructor called
```




