## <u>Constructors and Destructors</u>

### <u>Constructors</u>

A constructor is a particular member function having the same name as the class name. It calls automatically whenever the object of the class is created.

eg:-

```c++
#include <iostream.h>  
#include <conio.h>  
using namespace std;  
class hello {     // The class  
  public:           // Access specifier  
   hello () {     // Constructor  
      cout << "Hello World! Program in C++ by using Constructor";  
    }  
   void display() {  
     cout <<"Hello World!" <<endl;  
   }  
};  
int main() {  
  hello myObj;   /  
  return 0;  
}  
```

<b>There are four types of constructors used in C++.</b>

- Default constructor
- Dynamic constructor
- Parameterized constructor
- Copy constructor

#### Default constructor

A constructor is a class which accepts no parameter and is called a default constructor. If there is no constructor for a class, the compiler implicitly creates a default constructor.

```c++
class class_name {  
private:  
………..  
………..  
public:  
class_name ()  
{  
…….  
}  
} 
```

#### Parameterized constructor

A constructor is a class that can take parameters and is called a parameterized constructor. It is used to initialize objects with a different set of values.

```c++
Class classname  
{  
…………;  
…………;  
Public:  
Class name (parameter list)  
{  
………….;  
}  
}; 
```

#### Copy Constructor

A particular constructor used for the creation of an existing object. The copy constructor is used to initialize the thing from another of the same type.

```c++
Class (classname, &object)  
{  
………….;  
………….;  
}  
```

#### Dynamic constructor

This type of constructor can be used to allocate the memory while creating the objects. The data members of an object after creation can be initialized, called dynamic initialization.


### <u>Destructors</u>

Destructors have the same class name preceded by (~) tilde symbol. It removes and destroys the memory of the object, which the constructor allocated during the creation of an object.

eg:-

```c++
#include <iostream.h>  
#include <conio.h>  
using namespace std;  
class Hello {  
public:  
  //Constructor  
  Hello () {  
    cout<< "Constructor function is called" <<endl;  
  }  
  //Destructor  
  ~Hello () {  
    cout << "Destructor function is called" <<endl;  
   }  
   //Member function  
   void display() {  
     cout <<"Hello World!" <<endl;  
   }  
};  
int main(){  
   //Object created  
   Hello obj;  
   //Member function called  
   obj.display();  
   return 0;  
}  
```
### <u>Difference between Constructor and Destructor</u>

| Basis            | Constructor                                                    | Destructor                                                                                          |
|-----------------|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Purpose of use   | To allocate memory to the object                               | To deallocate the memory allocated by the constructor for the object                               |
| Arguments        | May or may not have arguments                                   | Does not have arguments                                                                             |
| Calling          | Automatically called when object of the class is created       | Automatically called when program terminates                                                       |
| Memory           | Occupies memory                                                 | Releases memory                                                                                     |
| Return type      | Has return type                                                 | Does not have return type                                                                           |
| Special symbol   | No special symbol required for declaration                      | The tilde symbol (~) is required in declaration                                                     |
| In numbers       | Multiple constructors can be used in a program                  | Only one destructor can be used in a program                                                        |
| Inheritance      | Can be inherited                                                | Cannot be inherited                                                                                 |
| Overloading      | Can be overloaded                                               | Cannot be overloaded                                                                                |
| Execution Order  | Executed in successive order                                    | Executed in reverse order of the constructors                                                       |
| Types            | Default constructor, copy constructor, parameterized constructor, dynamic constructor | No types for destructors                                                                        |
| Declaration      | ```class class_name {public: class_name([parameter list]) { }};``` | ```class class_name {public: ~xyz() { }};```                                                         |



