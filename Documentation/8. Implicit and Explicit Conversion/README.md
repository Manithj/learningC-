## <u>Implicit and Explicit Conversion</u>

In this topic, we will discuss the conversion of one data type into another in the C++ programming language. Type conversion is the process that converts the predefined data type of one variable into an appropriate data type. The main idea behind type conversion is to convert two different data type variables into a single data type to solve mathematical and logical expressions easily without any data loss.

Type conversion can be done in two ways in C++, one is <b>implicit type conversion</b>, and the second is <b>explicit type conversion</b>. Those conversions are done by the compiler itself, called the implicit type or automatic type conversion. The conversion, which is done by the user or requires user interferences called the explicit or user define type conversion.

### Implicit Type Conversion

The implicit type conversion is the type of conversion done automatically by the compiler without any human effort. It means an implicit conversion automatically converts one data type into another type based on some predefined rules of the C++ compiler. Hence, it is also known as the automatic type conversion.

```c++
#include <iostream>  
using namespace std;  
int main()  
{  
int num; // declare int type variable   
double num2 = 15.25; // declare and assign the double variable   
  
// use implicit type conversion to assign a double value to int variable  
num = num2;  
cout << " The value of the int variable is: " << num << endl;  
cout << " The value of the double variable is: " << num2 << endl;  
return 0;  
}  
```

Output

```
The value of the int variable is: 15
The value of the double variable is: 15.25
```

### Explicit type conversion

Conversions that require user intervention to change the data type of one variable to another, is called the explicit type conversion. In other words, an explicit conversion allows the programmer to manually changes or typecasts the data type from one variable to another type. Hence, it is also known as typecasting. Generally, we force the explicit type conversion to convert data from one type to another because it does not follow the implicit conversion rule.

The explicit type conversion is divided into two ways:

1.Explicit conversion using the cast operator<br>
2.Explicit conversion using the assignment operator

#### Program to convert float value into int type using the cast operator

```c++
#include <iostream>  
using namespace std;  
int main ()  
{  
float f2 = 6.7;  
// use cast operator to convert data from one type to another  
int x = static_cast <int> (f2);  
cout << " The value of x is: " << x;  
return 0;  
}   
```

Output

```
The value of x is: 6
```

#### Program to convert one data type into another using the assignment operator

```c++
#include <iostream>  
using namespace std;  
int main ()  
{  
// declare a float variable  
float num2;  
// initialize an int variable  
int num1 = 25;  
  
// convert data type from int to float  
num2 = (float) num1;  
cout << " The value of int num1 is: " << num1 << endl;  
cout << " The value of float num2 is: " << num2 << endl;  
return 0;  
}  
```

Output

```
The value of int num1 is: 25
The value of float num2 is: 25.0
```