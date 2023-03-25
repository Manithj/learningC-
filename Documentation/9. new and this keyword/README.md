## new and this keyword

### this keyword

In C++ programming, this is a keyword that refers to the current instance of the class. There can be 3 main usage of this keyword in C++.

- It can be used to pass current object as a parameter to another method.
- It can be used to refer current class instance variable.
- It can be used to declare indexers.

eg:-
```c++
#include <iostream>  
using namespace std;  
class Employee {  
public:  
    int id; //data member (also instance variable)      
    string name; //data member(also instance variable)  
    float salary;  
    Employee(int id, string name, float salary)    
    {    
	this->id = id;    
	this->name = name;    
	this->salary = salary;   
    }    
    void display()    
    {    
        cout<<id<<"  "<<name<<"  "<<salary<<endl;    
    }    
};  
int main(void) {  
    Employee e1 =Employee(101, "Sonoo", 890000); //creating an object of Employee   
    Employee e2=Employee(102, "Nakul", 59000); //creating an object of Employee  
    e1.display();    
    e2.display();    
    return 0;  
}  
```
Output

```
101  Sonoo  890000
102  Nakul  59000
```

### new keyword

The new operator is an operator which denotes a request for memory allocation on the Heap. If sufficient memory is available, new operator initializes the memory and returns the address of the newly allocated and initialized memory to the pointer variable. When you create an object of class using new keyword(normal new).

- The memory for the object is allocated using operator new from heap.
- The constructor of the class is invoked to properly initialize this memory.

```c++
#include<iostream>
using namespace std;
class car
{
string name;
int num;

public:
    car(string a, int n)
    {
        cout << "Constructor called" << endl;
        this ->name = a;
        this ->num = n;
    }

    void enter()
    {
        cin>>name;
        cin>>num;
    }

    void display()
    {
        cout << "Name: " << name << endl;
        cout << "Num: " << num << endl;
    }
};

int main()
{
	// Using new keyword
	car *p = new car("Honda", 2017);
	p->display();
}
```

Output

```
Constructor called
Name: Honda
Num: 2017
```
