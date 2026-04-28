# **C Language Code Compendium**

---

## **1\. printf (Formatted Output)**

**General Purpose:**  
Prints formatted output to the console.

**Example:**

\#include \<stdio.h\>

int main() {

    printf("Hello, world\!\\n");

    printf("Number: %d\\n", 42);

    return 0;

}

**Output:**

Hello, world\!

Number: 42

---

## **2\. scanf (Formatted Input)**

**General Purpose:**  
Reads formatted input from the user.

**Example:**

\#include \<stdio.h\>

int main() {

    int x;

    scanf("%d", \&x);

    printf("You entered: %d\\n", x);

    return 0;

}

**Output:**

(If user enters 5\)

You entered: 5

---

## **3\. if Statement**

**General Purpose:**  
Executes code conditionally.

**Example:**

\#include \<stdio.h\>

int main() {

    int x \= 10;

    if (x \> 5\) {

        printf("x is greater than 5\\n");

    }

    return 0;

}

**Output:**

x is greater than 5

---

## **4\. for Loop**

**General Purpose:**  
Repeats a block of code a fixed number of times.

**Example:**

\#include \<stdio.h\>

int main() {

    for (int i \= 0; i \< 3; i++) {

        printf("%d\\n", i);

    }

    return 0;

}

**Output:**

0

1

2

---

## **5\. while Loop**

**General Purpose:**  
Repeats code while a condition is true.

**Example:**

\#include \<stdio.h\>

int main() {

    int i \= 0;

    while (i \< 3\) {

        printf("%d\\n", i);

        i++;

    }

    return 0;

}

**Output:**

0

1

2

---

## **6\. Functions**

**General Purpose:**  
Encapsulates reusable blocks of code.

**Example:**

\#include \<stdio.h\>

int add(int a, int b) {

    return a \+ b;

}

int main() {

    printf("%d\\n", add(2, 3));

    return 0;

}

**Output:**

5

---

## **7\. Arrays**

**General Purpose:**  
Stores multiple values of the same type.

**Example:**

\#include \<stdio.h\>

int main() {

    int arr\[3\] \= {1, 2, 3};

    printf("%d\\n", arr\[1\]);

    return 0;

}

**Output:**

2

---

## **8\. Pointers**

**General Purpose:**  
Stores memory addresses and allows indirect access to variables.

**Example:**

\#include \<stdio.h\>

int main() {

    int x \= 10;

    int \*p \= \&x;

    printf("%d\\n", \*p);

    return 0;

}

**Output:**

10

---

## **9\. malloc (Dynamic Memory Allocation)**

**General Purpose:**  
Allocates memory at runtime.

**Example:**

\#include \<stdio.h\>

\#include \<stdlib.h\>

int main() {

    int \*p \= malloc(sizeof(int));

    \*p \= 7;

    printf("%d\\n", \*p);

    free(p);

    return 0;

}

**Output:**

7

---

## **10\. Structs**

**General Purpose:**  
Groups different data types into a single unit.

**Example:**

\#include \<stdio.h\>

struct Point {

    int x;

    int y;

};

int main() {

    struct Point p \= {3, 4};

    printf("%d %d\\n", p.x, p.y);

    return 0;

}

**Output:**

3 4

---

## **11\. File I/O (fopen, fprintf, fclose)**

**General Purpose:**  
Reads from and writes to files.

**Example:**

\#include \<stdio.h\>

int main() {

    FILE \*f \= fopen("test.txt", "w");

    fprintf(f, "Hello file\!\\n");

    fclose(f);

    return 0;

}

**Output:**

(File test.txt contains: Hello file\!)

---

## **12\. switch Statement**

**General Purpose:**  
Selects one of many code blocks to execute.

**Example:**

\#include \<stdio.h\>

int main() {

    int x \= 2;

    switch (x) {

        case 1: printf("One\\n"); break;

        case 2: printf("Two\\n"); break;

        default: printf("Other\\n");

    }

    return 0;

}

**Output:**

Two

---

## **13\. Strings (char arrays)**

**General Purpose:**  
Handles text using character arrays.

**Example:**

\#include \<stdio.h\>

int main() {

    char str\[\] \= "Hello";

    printf("%s\\n", str);

    return 0;

}

**Output:**

Hello

---

## **14\. strcmp (String Compare)**

**General Purpose:**  
Compares two strings.

**Example:**

\#include \<stdio.h\>

\#include \<string.h\>

int main() {

    if (strcmp("a", "b") \== 0\)

        printf("Equal\\n");

    else

        printf("Not equal\\n");

    return 0;

}

**Output:**

Not equal

---

## **15\. sizeof Operator**

**General Purpose:**  
Returns the size of a type or variable in bytes.

**Example:**

\#include \<stdio.h\>

int main() {

    printf("%zu\\n", sizeof(int));

    return 0;

}

**Output:**

(typically 4\)

---

## **16\. exit**

**General Purpose:**  
Terminates the program immediately.

**Example:**

\#include \<stdlib.h\>

int main() {

    exit(0);

}

**Output:**

(program exits)

---

## **17\. typedef**

**General Purpose:**  
Creates a new name for an existing type.

**Example:**

\#include \<stdio.h\>

typedef int myInt;

int main() {

    myInt x \= 5;

    printf("%d\\n", x);

    return 0;

}

**Output:**

5

---

## **18\. Enums**

**General Purpose:**  
Defines a set of named integer constants.

**Example:**

\#include \<stdio.h\>

enum Day {MON, TUE, WED};

int main() {

    enum Day d \= TUE;

    printf("%d\\n", d);

    return 0;

}

**Output:**

1

---

## **19\. const**

**General Purpose:**  
Defines read-only variables.

**Example:**

\#include \<stdio.h\>

int main() {

    const int x \= 10;

    printf("%d\\n", x);

    return 0;

}

**Output:**

10

---

## **20\. Command Line Arguments**

**General Purpose:**  
Accesses arguments passed to the program.

**Example:**

\#include \<stdio.h\>

int main(int argc, char \*argv\[\]) {

    printf("%s\\n", argv\[1\]);

    return 0;

}

**Output:**

(If run with: ./a.out hello)

hello

---

## **21\. fgets (Safe String Input)**

**General Purpose:**  
Reads a line of text safely from input (prevents buffer overflow).

**Example:**

\#include \<stdio.h\>

int main() {

    char str\[10\];

    fgets(str, sizeof(str), stdin);

    printf("%s", str);

    return 0;

}

**Output:**

(User enters: hi)

hi

---

## **22\. puts / gets (String Output/Input)**

**General Purpose:**  
Outputs a string (puts). Note: gets is unsafe and deprecated.

**Example:**

\#include \<stdio.h\>

int main() {

    puts("Hello");

    return 0;

}

**Output:**

Hello

---

## **23\. realloc**

**General Purpose:**  
Resizes previously allocated memory.

**Example:**

\#include \<stdio.h\>

\#include \<stdlib.h\>

int main() {

    int \*arr \= malloc(2 \* sizeof(int));

    arr \= realloc(arr, 4 \* sizeof(int));

    free(arr);

    return 0;

}

**Output:**

(memory resized)

---

## **24\. calloc**

**General Purpose:**  
Allocates and initializes memory to zero.

**Example:**

\#include \<stdlib.h\>

int main() {

    int \*arr \= calloc(3, sizeof(int));

    free(arr);

    return 0;

}

**Output:**

(memory initialized to 0\)

---

## **25\. Pointer Arithmetic**

**General Purpose:**  
Allows traversal of memory using pointers.

**Example:**

\#include \<stdio.h\>

int main() {

    int arr\[3\] \= {1,2,3};

    int \*p \= arr;

    printf("%d

", \*(p \+ 1));

    return 0;

}

**Output:**

2

---

## **26\. Double Pointers**

**General Purpose:**  
Stores address of another pointer.

**Example:**

\#include \<stdio.h\>

int main() {

    int x \= 5;

    int \*p \= \&x;

    int \*\*pp \= \&p;

    printf("%d

", \*\*pp);

    return 0;

}

**Output:**

5

---

## **27\. Function Pointers**

**General Purpose:**  
Stores functions as variables.

**Example:**

\#include \<stdio.h\>

int add(int a, int b) {

    return a \+ b;

}

int main() {

    int (\*f)(int,int) \= add;

    printf("%d

", f(2,3));

    return 0;

}

**Output:**

5

---

## **28\. Bitwise AND (&)**

**General Purpose:**  
Performs bitwise AND operation.

**Example:**

\#include \<stdio.h\>

int main() {

    printf("%d

", 5 & 3);

    return 0;

}

**Output:**

1

---

## **29\. Bitwise OR (|)**

**General Purpose:**  
Performs bitwise OR operation.

**Example:**

\#include \<stdio.h\>

int main() {

    printf("%d

", 5 | 3);

    return 0;

}

**Output:**

7

---

## **30\. Bitwise XOR (^)**

**General Purpose:**  
Performs bitwise XOR operation.

**Example:**

\#include \<stdio.h\>

int main() {

    printf("%d

", 5 ^ 3);

    return 0;

}

**Output:**

6

---

## **31\. Bitwise NOT (\~)**

**General Purpose:**  
Inverts all bits.

**Example:**

\#include \<stdio.h\>

int main() {

    printf("%d

", \~5);

    return 0;

}

**Output:**

\-6

---

## **32\. Left Shift (\<\<)**

**General Purpose:**  
Shifts bits left.

**Example:**

\#include \<stdio.h\>

int main() {

    printf("%d

", 1 \<\< 3);

    return 0;

}

**Output:**

8

---

## **33\. Right Shift (\>\>)**

**General Purpose:**  
Shifts bits right.

**Example:**

\#include \<stdio.h\>

int main() {

    printf("%d

", 8 \>\> 2);

    return 0;

}

**Output:**

2

---

## **34\. Preprocessor \#define**

**General Purpose:**  
Defines macros or constants.

**Example:**

\#include \<stdio.h\>

\#define PI 3.14

int main() {

    printf("%.2f

", PI);

    return 0;

}

**Output:**

3.14

---

## **35\. Conditional Compilation (\#ifdef)**

**General Purpose:**  
Compiles code conditionally.

**Example:**

\#include \<stdio.h\>

\#define DEBUG

int main() {

\#ifdef DEBUG

    printf("Debug mode

");

\#endif

    return 0;

}

**Output:**

Debug mode

---

## **36\. static Keyword**

**General Purpose:**  
Preserves variable value between function calls.

**Example:**

\#include \<stdio.h\>

void counter() {

    static int count \= 0;

    count++;

    printf("%d

", count);

}

int main() {

    counter();

    counter();

    return 0;

}

**Output:**

1

2

---

## **37\. extern Keyword**

**General Purpose:**  
Declares a global variable defined elsewhere.

**Example:**

\#include \<stdio.h\>

extern int x;

int x \= 5;

int main() {

    printf("%d

", x);

    return 0;

}

**Output:**

5

---

## **38\. Union**

**General Purpose:**  
Stores different data types in the same memory location.

**Example:**

\#include \<stdio.h\>

union Data {

    int i;

    float f;

};

int main() {

    union Data d;

    d.i \= 10;

    printf("%d

", d.i);

    return 0;

}

**Output:**

10

---

## **39\. volatile Keyword**

**General Purpose:**  
Prevents compiler optimization on variables.

**Example:**

volatile int x;

**Output:**

(no direct output)

---

## **40\. goto**

**General Purpose:**  
Jumps to a labeled statement.

**Example:**

\#include \<stdio.h\>

int main() {

    goto skip;

    printf("This won't print

");

skip:

    printf("Skipped

");

    return 0;

}

**Output:**

Skipped

---

## **41\. printf Format Specifiers (DEBUG ESSENTIAL)**

**General Purpose:**  
Provides all common format specifiers used to print different data types.

**Example:**

\#include \<stdio.h\>

int main() {

    int i \= 10;

    float f \= 3.14;

    double d \= 3.1415926535;

    char c \= 'A';

    char \*s \= "hello";

    void \*p \= \&i;

    printf("int: %d", i);

    printf("float: %f", f);

    printf("double: %lf", d);

    printf("char: %c", c);

    printf("string: %s", s);

    printf("pointer: %p", p);

    return 0;

}

**Output:**

int: 10

float: 3.140000

double: 3.141593

char: A

string: hello

pointer: (address)

**Common Specifiers Cheat Sheet:**

%d  \-\> int

%f  \-\> float

%lf \-\> double

%c  \-\> char

%s  \-\> string (char\*)

%p  \-\> pointer

%u  \-\> unsigned int

%lu \-\> unsigned long

%ld \-\> long

%lld-\> long long

%x  \-\> hex

%d \-\> bool

	or the following for text:

printf("%s\\n", my\_bool ? "true" : "false");

---

## **42\. Type Debugging with sizeof \+ printf**

**General Purpose:**  
Helps identify type sizes and debug memory layout.

**Example:**

\#include \<stdio.h\>

int main() {

    printf("int: %zu

", sizeof(int));

    printf("float: %zu

", sizeof(float));

    printf("double: %zu

", sizeof(double));

    printf("pointer: %zu

", sizeof(void\*));

    return 0;

}

**Output:**

int: 4

float: 4

double: 8

pointer: 8

---

## **43\. Printing Memory Addresses**

**General Purpose:**  
Helps debug pointer issues and memory layout.

**Example:**

\#include \<stdio.h\>

int main() {

    int x \= 5;

    printf("Address of x: %p

", \&x);

    return 0;

}

**Output:**

Address of x: (memory address)

---

## **44\. Casting (Type Conversion)**

**General Purpose:**  
Forces a variable into another type (useful for debugging and correctness).

**Example:**

\#include \<stdio.h\>

int main() {

    int x \= 5;

    double y \= (double)x / 2;

    printf("%f

", y);

    return 0;

}

**Output:**

2.500000

---

## **45\. Format Precision and Width**

**General Purpose:**  
Controls output formatting for debugging values precisely.

**Example:**

\#include \<stdio.h\>

int main() {

    float f \= 3.14159;

    printf("%.2f

", f);

    printf("%10d

", 42);

    return 0;

}

**Output:**

3.14

        42

---

## **46\. Debug Macro**

**General Purpose:**  
Quick debugging prints with file and line info.

**Example:**

\#include \<stdio.h\>

\#define DEBUG\_PRINT(x) printf("DEBUG %s:%d \-\> %s \= %d

", \_\_FILE\_\_, \_\_LINE\_\_, \#x, x)

int main() {

    int a \= 5;

    DEBUG\_PRINT(a);

    return 0;

}

**Output:**

DEBUG file.c:line \-\> a \= 5

---

## **47\. \_Generic (Type Detection in C11)**

**General Purpose:**  
Determines type at compile-time (advanced debugging tool).

**Example:**

\#include \<stdio.h\>

\#define TYPEOF(x) \_Generic((x), \\

    int: "int", \\

    float: "float", \\

    double: "double", \\

    char\*: "string", \\

    default: "other")

int main() {

    int x \= 5;

    printf("%s

", TYPEOF(x));

    return 0;

}

**Output:**

int

---

## **48\. fprintf to stderr (Debug Output)**

**General Purpose:**  
Separates debug logs from normal output.

**Example:**

\#include \<stdio.h\>

int main() {

    fprintf(stderr, "Debug message

");

    return 0;

}

**Output:**

(goes to stderr)

---

## **49\. assert**

**General Purpose:**  
Checks assumptions during debugging.

**Example:**

\#include \<assert.h\>

int main() {

    int x \= 5;

    assert(x \== 5);

    return 0;

}

**Output:**

(no output if true, crash if false)

---

## **50\. perror**

**General Purpose:**  
Prints descriptive error messages based on errno.

**Example:**

\#include \<stdio.h\>

int main() {

    FILE \*f \= fopen("missing.txt", "r");

    if (\!f) perror("Error");

    return 0;

}

**Output:**

Error: (system message)

# 

## 51\. comparing strings

**general purpose:**  
compare strings

**example:**

\#include \<stdio.h\>  
\#include \<string.h\>

int main() {  
    char s1\[\] \= "hello";  
    char s2\[\] \= "hello";

    if (strcmp(s1, s2) \== 0\) {  
        printf("Strings are equal\\n");  
    }  
    return 0;  
}

## 52\. empty strings

In C, an empty string is a character array where the very first element is the null terminator ('\\0'). Because C defines a string as a sequence of characters followed by a null byte, an empty string contains no "visible" characters and has a length of zero. 

