## Arrow operator ->

An Arrow operator in C/C++ allows to access elements in Structures and Unions. It is used with a pointer variable pointing to a structure or union. The arrow operator is formed by using a minus sign, followed by the greater than symbol as shown below. 

`(pointer_name)->(variable_name)`

### Difference between Dot(.) and Arrow(->) operator <br>

- The Dot(.) operator is used to normally access members of a structure or union.
- The Arrow(->) operator exists to access the members of the structure or the unions using pointers.

### Arrow operator in structure

```c++
// C++ program to show Arrow operator
// used in structure
#include <iostream>
using namespace std;

// Creating the structure
struct student {
	char name[80];
	int age;
	float percentage;
};

// Creating the structure object
struct student* emp = NULL;

// Driver code
int main()
{

	// Assigning memory to struct variable emp
	emp = (struct student*)malloc(sizeof(struct student));

	// Assigning value to age variable
	// of emp using arrow operator
	emp->age = 18;

	// Printing the assigned value to the variable
	cout <<" "<< emp->age;

	return 0;
}
```

Output

```
18
```

### Arrow operator in unions

```c++
// C++ program to show Arrow operator
// used in structure
#include <iostream>
using namespace std;

// Creating the union
union student {
	char name[80];
	int age;
	float percentage;
};

// Creating the union object
union student* emp = NULL;

// Driver code
int main()
{
	// Assigning memory to struct variable emp
	emp = (union student*)
		malloc(sizeof(union student));

	// Assigning value to age variable
	// of emp using arrow operator
	emp->age = 18;

	// DIsplaying the assigned value to the variable
	cout <<""<< emp->age;
}
```

Output

```
18
```

