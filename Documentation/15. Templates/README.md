## Templates

A C++ template is a powerful feature added to C++. It allows you to define the generic classes and generic functions and thus provides support for generic programming. Generic programming is a technique where generic types are used as parameters in algorithms so that they can work for a variety of data types.

Templates can be represented in two ways

- Function template - We can define a template for a function. For example, if we have an add() function, we can create versions of the add function for adding the int, float or double type values.

- Class templates   - We can define a template for a class. For example, a class template can be created for the array class that can accept the array of various types such as int array, float array or double array.

### Function Template

- Generic functions use the concept of a function template. Generic functions define a set of operations that can be applied to the various types of data.

- The type of the data that the function will operate on depends on the type of the data passed as a parameter.

- For example, Quick sorting algorithm is implemented using a generic function, it can be implemented to an array of integers or array of floats.

- A Generic function is created by using the keyword template. The template defines what function will do.

<b>Syntax of Function Template</b>

```c++
template < class Ttype> 
Ttype func_name(parameter_list)  
{  
    // body of function.  
}  
```

Where `Ttype`: It is a placeholder name for a data type used by the function. It is used within the function definition. It is only a placeholder that the compiler will automatically replace this placeholder with the actual data type.

`class` A class keyword is used to specify a generic type in a template declaration.

`typename` also can be used to specify a generic type in a template declaration.



<b>example of a function template</b>

```c++
#include <iostream>  
using namespace std;  
template<class T> T add(T &a,T &b)  
{  
	T result = a+b;  
	return result;  
      
}  
int main()  
{  
  int i =2;  
  int j =3;  
  float m = 2.3;  
  float n = 1.2;  
  cout<<"Addition of i and j is :"<<add(i,j);  
  cout<<'\n';  
  cout<<"Addition of m and n is :"<<add(m,n);  
  return 0;  
}  
```

Output

```
Addition of i and j is :5
Addition of m and n is :3.5
```

<b>Function Templates with Multiple Parameters</b>

eg:-

```c++
#include <iostream>  
using namespace std;  
template<class X,class Y> void fun(X a,Y b)  
{  
	std::cout << "Value of a is : " <<a<< std::endl;  
	std::cout << "Value of b is : " <<b<< std::endl;  
}  
  
int main()  
{  
	fun(15,12.3);  
	return 0;  
}  
```

Output

```
Value of a is : 15
Value of b is : 12.3
```

### Class Template

Class Template can also be defined similarly to the Function Template. When a class uses the concept of Template, then the class is known as generic class.

eg:-

```c++
#include <iostream>  
using namespace std;  
template<class T>  
class A   
{  
	public:  
	T num1 = 5;  
	T num2 = 6;  
	void add()  
	{  
			std::cout << "Addition of num1 and num2 : " << num1+num2<<std::endl;  
	}  
      
};  
  
int main()  
{  
	A<int> d;  
	d.add();  
	return 0;  
}  
```

Output

```
Addition of num1 and num2 : 11
```

<b>example when class template contains two generic data types.</b>

```c++
#include <iostream>  
using namespace std;  
template<class T1, class T2>  
class A   
	{  
	T1 a;  
	T2 b;  
	public:  
		A(T1 x,T2 y)  
		{  
			a = x;  
			b = y;  
		}  
		void display() 
		{  
			std::cout << "Values of a and b are : " << a<<" ,"<<b<<std::endl;  
		}  
	};  

int main()  
{  
	A<int,float> d(5,6.5);  
	d.display();  
	return 0;  
}  
```

Output

```
Values of a and b are : 5,6.5
```




