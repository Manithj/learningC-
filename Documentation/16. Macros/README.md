## Macros

A C++ macro is defined as a section of code that that particular macro value can replace. We can define the macro by using a `#define` directive. When the compiler goes to the macros while program compilation, the macro's name is replaced by the definition of the macro. The termination of the C++ Macros does not need a semi-colon (;).

eg:-

```c++

#include <iostream>
using namespace std;
 
// Here is the definition of macro.
#define AREA(l, b) (l * b)

int main() {
	// The given lengths are l1 and l2.
	int l1 = 20, l2 = 2, area;

	// Here, finding the area using macro.
	area = AREA(l1, l2);

	
	cout << "Area of the rectangle" << " is: "<< area;

	return 0;
}
```
Output

```
Area of the rectangle is: 40
```

In the above code, we are computing the area of the rectangle by AREA macro that receives the user's input for the rectangle's length and width before calculating the area. Two integer variables with their respective values are declared in the main class. When the AREA macro is used in the main class, it will accept integer numbers as input and do the calculation following the macro's logic. Finally, the output gets printed out.

### Types of Macros

### 1.Chain Macros

As the name suggests, chain macros are defined as macros inside the macros. In the chain macro, the parent macro is expanded first, and then its child macros.

```c++
#include <iostream>
using namespace std;
 
// Macro definition.
#define FACEBOOK FOLLOWERS
#define FOLLOWERS 150
 
// Main Code.
int main() {
    
	cout << " This user have "<< FACEBOOK << "K followers on Facebook!";
 	return 0;
}
```

Output

```
This user have 150K followers on Facebook!
```

### 2.Object-Like Macros

The object-like macro is an identifier that gets replaced by code fragments. This macro is given the name object-like macro because the code segment looks like an object of code. This type of macro is generally used to replace a symbolic name with the variable being represented as a constant.

```c++
#include <iostream>
using namespace std;
 
// Definition of Macro.
#define DATE 25
 
// Main Code.
int main() {
	// Here, the message will be printed.
	cout << "The lockdown is extended upto "<< DATE << "-JUNE-2020";

	return 0;
}
```

Output

```
The lockdown is extended upto25-JUNE-2020
```

### 3.Function-like Macros

The function-like macro is almost similar to the function call in a program. In it, the whole code is replaced by a function name. Since it is similar to function, there must be a pair of parentheses after the macro's name. We should never put a space between the macro name and the parentheses in the macro definition.

```c++

#include <iostream>
using namespace std;
 
//  Definition of the macro.
#define min(x, y) (((x) < (y)) ? (x) : (y))
 
// Main Code.
int main() {
 
    int x = 21;
    int y = 56;
 
    cout << "The minimum value between " << x << " and " << y
         << " is: " << min(x, y);
 
    return 0;
}
```

Output

```
The minimum value between 21 and 56 is: 21
```

### 4.Multi-Line Macros

A multi-line macro contains more than one line of definition in it. We create a multi-line macro by the use of backslash '\'.

```c++

#include <iostream>
using namespace std;
 
//  Definition of Multi-line Macro.
#define ABA 1, \
            2, \
            3
 
// Main Code.
int main() {
	// Array arr[] with elements defined in macro 'ABA'.
	int arr[] = { ABA };

	cout<<"Elements of Array are:\n";

	for (int i = 0; i < 3; i++) {
			cout << arr[i] << ' ';
	}

	return 0;
}
```

Output

```
Elements of Array are:
1 2 3 
```