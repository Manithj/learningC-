## <u>Classes vs Struct</u>

### <u>C++ Class</u>

In C++, class is a group of similar objects. It is a template from which objects are created. It can have fields, methods, constructors etc.

eg:-
```c++
class Student    
 {    
     public:  
     int id;  //field or data member     
     float salary; //field or data member  
     String name;//field or data member    
 }
 ```

 C++ object class

 ```c++
#include <iostream>  
using namespace std;  
   class Student {  
      public:  
         int id;//data member (also instance variable)      
         string name;//data member(also instance variable)      
   };  
   int main() {  
      Student s1; //creating an object of Student   
      s1.id = 201;    
      s1.name = "Sonoo Jaiswal";   
      cout<<s1.id<<endl;  
      cout<<s1.name<<endl;  
      return 0;  
   } 
```

Output

```
201
Sonoo Jaiswal
```

### <u>C++ Structs</u>

In C++, classes and structs are blueprints that are used to create the instance of a class. Structs are used for lightweight objects such as Rectangle, color, Point, etc.

Unlike class, structs in C++ are value type than reference type. It is useful if you have data that is not intended to be modified after creation of struct.

C++ Structure is a collection of different data types. It is similar to the class that holds different types of data.

eg:-

```C++
#include <iostream>    
using namespace std;    
 struct Rectangle      
{      
   int width, height;      
      
 };      
int main(void) {    
    struct Rectangle rec;    
    rec.width=8;    
    rec.height=5;    
   cout<<"Area of Rectangle is: "<<(rec.width * rec.height)<<endl;    
 return 0;    
} 
```
Output

```
Area of Rectangle is: 40
```

#### C++ Struct Example: Using Constructor and Method

```c++
#include <iostream>    
using namespace std;    
 struct Rectangle    {      
   int width, height;      
  Rectangle(int w, int h)      
    {      
        width = w;      
        height = h;      
    }      
  void areaOfRectangle() {       
    cout<<"Area of Rectangle is: "<<(width*height); }      
 };      
int main(void) {    
    struct Rectangle rec=Rectangle(4,6);    
    rec.areaOfRectangle();    
   return 0;    
}
```

Output

```
Area of Rectangle is: 24
```

### Difference between Classes & Struct

|Class |Structure |
|:--- |:--- |
|If access specifier is not declared explicitly, then by default access specifier will be private.|If access specifier is not declared explicitly, then by default access specifier will be public.|
|Syntax of Class:<br>class class_name<br>{<br>// body of the class.<br>}|Syntax of Structure:<br>struct structure_name<br>{<br>// body of the structure.<br>}|
|The instance of the class is known as "Object of the class".|The instance of the structure is known as "Structure variable".|
|It is normally used for data abstraction and further inheritance.|It is normally used for the grouping of data|
|NULL values are possible in Class.|NULL values are not possible.|
