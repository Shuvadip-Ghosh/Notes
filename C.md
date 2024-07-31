# C Language Cheat Sheet
This C cheatsheet is aimed to provide you with a quick syntax revision of C language. This will be helpful for students who need a quick syntax revision right before their exams or professionals to quickly look at the C language syntax. Let's start with the basics and move toward the more intricate aspects of C programming.
## Basics
Basic syntax and functions from the C programming language.
### Boilerplate Code
```c
#include<stdio.h> //header files
int main() //main function
{
    // Your code here
    return(0); //returning value to int main()
}
```
### printf function
It is used to show output on the screen
```c
printf("Hello World!");
```
### scanf function
It is used to take input from the user
```c
scanf("format_specifier", &variables)
```
We use & with the variable name to represent "address of". This is how the syntax works:
```c
int a;
scanf("%d",&a); // Store keyboard input in a variable with address (address of a or &a)
printf("%d",a);
```
## Comments
A comment is a code that is not executed by the compiler, and the programmer uses it to annotate their code, providing explanations or reminders about the code's functionality, which aids in readability and future maintenance.
### Single line comment
```c
// This is a single line comment
```
### Multi-line comment
```c
/* This is a 
multi-line
comment
*/
```
## Data types
The data type defines the kind of data that can be stored in a variable, such as integers, floating-point numbers, characters, or more complex structures. It dictates how the data is stored, interpreted, and manipulated within the program.

### Character type
The character type, often represented as a single octet (one byte), is used to store individual characters in the C programming language.

```c
char variable_name;
```

The format specifier for a character in C is "%c". To print a character, we use this specifier within the `printf` function, following the syntax like this:

```c
char x;
scanf(" %c",&x);
printf("character is %c",x)
```
### Integer type
To store non-decimal numeric values, an integer type is used

```c
int variable_name;
```

The format specifier of an integer is "%d"

```c
int a;
scanf("%d",&a);
printf("%d",a);
```
### Float type
To store decimal numeric values, float type is used

```c
float variable_name;
```

The format specifier of a float is "%f"

```c
float b;
scanf("%f",&b);
printf("%f",b);
```
### Double type
To store a double-precision floating-point value we use double.

```c
double variable_name;
```

The format specifier of double is "%f"

```c
double ch;
scanf("%lf",&ch);
printf("%lf",ch);
```
### Void type

The void type in C represents the absence of a type. It's often used in function declarations to specify that the function does not return any value. For example:

```c
void myFunction() {
  // Function code here
}
```
In this context, the `void` keyword indicates that `myFunction` does not return a value. It can also be used for function parameters to indicate that a function takes no arguments

## Escape Sequences

Escape sequences in C are combinations of characters that begin with a backslash (`\`) and are used to represent characters that cannot be typed directly. These sequences are interpreted in a special way when used inside string literals or character constants.

For example, the escape sequence `\n` represents a newline character, and `\t` represents a tab character. Here are some escape sequence characters used in C language.

### Alarm or Beep
\a produces a beep sound
```c
#include<stdio.h>
int main()
{
    printf("\a"); // It produces a beep sound
    return 0;
}
```
### Backspace

\b adds a backspace

```c
#include<stdio.h>
int main()
{
    printf("Hello\bWorld"); // It prints "HellWorld"
    return 0;
}
```
### Form feed

```c
#include<stdio.h>
int main()
{
    printf("Page break here\fContinue text"); // It may create a page break, but it's not supported everywhere
    return 0;
}
```
### Newline
Newline Character

```c
#include<stdio.h>
int main()
{
    printf("Line one\nLine two"); // Prints two lines
    return 0;
}
```
### Carriage return

The carriage return, represented by the escape sequence `\r` in the C programming language, is a control character that resets the cursor position to the beginning of the current line. It doesn't erase any characters but simply moves the cursor to the start of the line. The string "Hello" is printed first, then the carriage return moves the cursor back to the beginning of the line, and "World" is printed, overwriting "Hello."

```c
#include<stdio.h>
int main()
{ 
    printf("Hello\rWorld"); // Outputs "World" but behavior might vary depending on the OS
    return 0;
}
```
### Tab

It gives a tab space

```c
#include<stdio.h>
int main()
{
    printf("Tabbed\ttext"); // Adds a tab space
    return 0;
}
```
### Backslash

It adds a backslash

```c
#include<stdio.h>
int main()
{
    printf("\\"); // Prints a backslash
    return 0;
}
```
### Single quote

It adds a single quotation mark

```c
#include<stdio.h>
int main()
{
    printf("\'"); // Prints a single quotation mark
    return 0;
}
```
### Question mark

It adds a question mark

```c
#include<stdio.h>
int main()
{
    printf("\?"); // Prints a question mark
    return 0;
}
```
### Octal No.

It represents the value of an octal number

```c
#include<stdio.h>
int main()
{
    printf("\101"); // Prints 'A', which is 101 in octal
    return 0;
}
```
### Hexadecimal No.

It represents the value of a hexadecimal number

```c
#include<stdio.h>
int main()
{
    printf("\x41"); // Prints 'A', which is 41 in hexadecimal
    return 0;
}
```
### Null

The null character is usually used to terminate a string

```c
#include<stdio.h>
int main()
{
    printf("\0");
    char str[] = "Hello\0World"; // The null character is used to terminate a string
    return 0;
}
```
## Conditional Instructions

Conditional statements are used to perform operations based on some condition.
### If Statement

```c
if (/* condition */)
{
    /* code */
}
```
### If-else Statement

```c
if (/* condition */)
{
    /* code */
}
else{
    /* Code */
}
```
### if else-if Statement

```c
if (condition) {
    // Statements;
}
else if (condition){
    // Statements;
}
else{
    // Statements
}
```
### nested if-else

```c
if (/* condition */) {
    if (/* condition */) {
        /* code */
    } else {
        /* Code */
    }
} else {
    /* Code */
}
```
### Switch Case Statement

It allows a variable to be tested for equality against a list of values (cases).

```c
switch (expression) {
    case constant-expression:
        statement1;
        statement2;
        break;
    case constant-expression:
        statement;
        break;
    // ...
    default:
        statement;
}
```
## Iterative Statements

Iterative statements facilitate programmers to execute any block of code lines repeatedly and can be controlled as per conditions added by the programmer.
### while Loop

It allows the execution of statements inside the block of the loop until the condition of the loop succeeds.

```c
while (/* condition */)
{
    /* code */
}
```
### do-while loop

It is an exit-controlled loop. It is very similar to the while loop with one difference, i.e., the body of the do-while loop is executed at least once even if the expression is false

```c
do
{
    /* code */
} while (/* condition */);
```
### for loop

It is used to iterate the statements or a part of the program several times. It is frequently used to traverse the data structures like the array and linked list.

```c
for (int i = 0; i < count; i++)
{
    /* code */
}
```
### Break Statement

break keyword inside the loop is used to terminate the loop

```c
#include <stdio.h>

int main() {
    for (int i = 0; i < 10; i++) {
        if (i == 5) {
            printf("Loop is breaking at i = 5\n");
            break; // Exit the loop when i is 5
        }
        printf("i = %d\n", i);
    }

    return 0;
}
```

Here is the output of the above code:

```c
i = 0
i = 1
i = 2
i = 3
i = 4
Loop is breaking at i = 5
```
### Continue Statement

continue keyword skips the rest of the current iteration of the loop and returns to the starting point of the loop

```c
#include <stdio.h>

int main() {
    for (int i = 1; i <= 10; i++) {
        if (i % 2 == 0) {
            continue; // Skip the rest of the loop body if i is even
        }
        printf("%d ", i); // Print the odd numbers
    }
    return 0;
}

// Output is 1 3 5 7 9
```
## Functions & Recursion

Functions are used to divide an extensive program into smaller pieces. It can be called multiple times to provide reusability and modularity to the C program.

### Function Definition

```c
return_type function_name(data_type parameter...){ 
//code to be executed 
}
```
### Function Call

```c
function_name(parameters...);
```
### return_type in functions

The function return statement returns the specified value or data item to the caller. If we do not want to return any value simply place a void before the function name while defining it.

```c
return_type function_name()
{
    return value;
}
```
### Parameters in C function

Parameters are the values passed inside the parenthesis of the function while defining as well as while calling.

```c
return_type function_name(data_type parameter...){    //defining the functions with parameters
    //code to be executed 
}
function_name(parameter...);    //calling the functions with parameters
```
### Ways of calling a function

1. With return value and with parameters
2. Without return value and with parameters
3. With return value and without parameters
4. Without return value and without parameters
### Recursion

Recursion is when a function calls a copy of itself to work on a minor problem. And the function that calls itself is known as the Recursive function.

```c
void recurse()
{
    ... .. ...
    recurse();
    ... .. ...
}
```
## Pointers

A pointer is a variable that contains the address of another variable,
### Declaration

```c
datatype *var_name;
```

We can allocate the address of the pointing variable to the pointer variable

```c
#include <stdio.h>

int main() {
    int *ptr, x;
    x = 15;
    ptr = &x;

    // This will print the address of x, not the value 15
    printf("%p", ptr);

    return 0;
}
 
```
### Dereferencing pointer variable

```c
#include <stdio.h>

int main() {
    int *ptr, x;
    x = 12;
    ptr = &x; // Assign the address of x to ptr
    printf("%d", *ptr); // Dereference ptr to print the value of x

    return 0;
}
```
## Arrays
An array is a collection of data items of the same type.
### Declaration

```c
data_type array_name[array_size];
```

```c
#include<stdio.h>                         
int main()                               
{
int arr[10];   
}
```

### Accessing element

```c
data_type variable_name = array[index];
```
## Strings

A string is a 1-D character array terminated by a null character ('\0')
### Declaration

```c
char str_name[size];
```
### gets() function

It allows you to enter a multi-word string.

```c
gets("string");
```
### puts() function

It is used to show string output

```c
puts("string");
```
### fgets() function

The `gets()` function is considered unsafe, and it is better to use `fgets()` instead.

```c
#include <stdio.h>

int main() {
    char str[50];
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    printf("You entered: %s", str);
    return 0;
}
```
### String Functions

### strlen() function

It is used to calculate the length of the string

```c
strlen(string_name);
```
### strcpy() function

It is used to copy the content of second-string into the first string passed to it

```c
strcpy(destination, source);
```
### strcat() function

It is used to concatenate two strings

```c
strcat(first_string, second_string);
```
### strcmp() function

It is used to compare two strings

```c
strcmp(first_string, second_string);
```
### strlwr() function

It is used to convert characters of strings into lowercase

```c
strlwr(string_name);
```
### strupr() function

It is used to convert characters of strings into uppercase

```c
strupr(string_name);
```
### strrev() function

It is used to reverse the string

```c
strrev(string_name);
```
## Structures

The structure is a collection of variables of different types under a single name. Defining structure means creating a new data type.
### Structure syntax

```c
struct structureName 
{
    dataType member1;
    dataType member2;
    ...
};
```
### typedef keyword

typedef function allows users to provide alternative names for the primitive and user-defined data types.

```c
typedef struct structureName 
{
    dataType member1;
    dataType member2;
    ...
} new_name;
```
## File Handling

A set of methods for handling File IO (read/write/append) in C language
### FILE pointer

```c
FILE *filePointer;
```
### Opening a file

It is used to open a file in C.

```c
filePointer = fopen(fileName.txt, w)
```
### fscanf() function

It is used to read the content of a file.

```c
fscanf(FILE *stream, const char *format, ...)
```
### fprintf() function

It is used to write content into the file.

```c
fprintf(FILE *fptr, const char *str, ...);
```
### fgetc() function

It reads a character from a file opened in read mode. It returns EOF on reaching the end of the file.

```c
fgetc(FILE *pointer);
```
### fputc() function

It writes a character to a file opened in write mode

```c
fputc(char, FILE *pointer);
```
### Closing a file

It closes the file.

```c
fclose(filePointer);
```
## Dynamic Memory Allocation

A set of functions for dynamic memory allocation from the heap. These methods are used to use the dynamic memory which makes our C programs more efficient

### malloc() function

Stands for 'Memory allocation' and reserves a block of memory with the given amount of bytes.

```c
ptr = (castType*) malloc(size);
```
### calloc() function

Stands for 'Contiguous allocation' and reserves n blocks of memory with the given amount of bytes.

```c
ptr = (castType*)calloc(n, size);
```
### free function

It is used to free the allocated memory.

```c
free(ptr);
```
### realloc() function

If the allocated memory is insufficient, then we can change the size of previously allocated memory using this function for efficiency purposes

```c
ptr = realloc(ptr, x);
```
