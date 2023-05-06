## Boilerplate
```java
class HelloWorld{
        public static void main(String args[]){
        }
}
```
## Print statement
```java
System.out.println("Hello World");
```
## Comments
```java
// It's a single line comment
/* It's a 
multi-line
comment
*/
```
## Data Types

### Primitive Data Types
```markdown
1. byte
2. short
3. int 
4. long
5. float
6. double
7. char
8. boolean
```
### Non-Primitive Data Types
```markdown
1. Strings
2. Array
3. Classes
4. Interface
```
## Taking Input

```java
import java.util.Scanner;
class HelloWorld
{
        public static void main(String args[])
        {
              Scannner sc=new Scanner(System.in);
              //String
              String name=sc.nextLine();
              System.out.println(name);
        }
}
```
#### String
```java
String name = sc.next(); // for string Input of First word
```
#### Char
```java
char c = sc.next().charAt(0); // taking first character as input
```
#### int
```java
int x=sc.nextInt();
```
#### Float
```java
int x=sc.nextFloat();
```
#### Double
```java
double x=sc.nextDouble();
```

## Escape Sequence

### Tab
```java
public class HelloWorld{
   public static void main(String args[]){
        System.out.print("\t");
   }
}
```
### Backslash
```java
public class HelloWorld{
   public static void main(String args[]){
        System.out.print("\\");
   }
}
```

### Single Quote
```java
public class HelloWorld{
   public static void main(String args[]){
        System.out.print("\'");
   }
}
```

## Type Casting
##### Automatic
```java
class HelloWorld{
   public static void main(String args[]){
        int x = 45;
        double var_name = x;
        System.out.println(var_name);
   }   
}
```
##### Manual
```java
int myInt = (int) myDouble;
```

## Conditional Statement
### if Statement
```java
if (condition) {
// block of code to be executed if the condition is true
}
```
### if else Statement
```java
if (condition) {
// If condition is True then this block will get executed
} else {
// If condition is False then this block will get executed
}
```
### if else-if Statement
```java
if (condition1) {
// Codes
}
else if(condition2) {
// Codes
}
else if (condition3) {
// Codes
}
else {
// Codes
}
```
### Ternery Operator
```java
variable = (condition) ? expressionForTrue : expressionForFalse;
```
### Switch Case
```java
class SwitchExample{
	public static void main(String args[]){
		int day = 4;
	    switch (day) {
		    case 1:
			    System.out.println("Monday");
			    break;
		    case 2:
			    System.out.println("Tuesday");
			    break;
		    case 3:
			    System.out.println("Wednesday");
			    break;
			 case 4:
			    System.out.println("Thursday");
				break;
			default:
				// code when none of The Cases satisfy
		}
	}
}
```

## Iterative Statements
### while Loop
```java
public class WhileExample
{  
  public static void main(String[] args) 
  {  
    int i=1;  
    while(i<=10)
    {  
        System.out.println(i);  
        i++;  
    }  
  }  
} 
```
### for Loop
```java
class HelloWorld
{
   public static void main(String args[])
   {
        int i;
        for(i=1;i<100;i++)
         {
              System.out.println(i);
         }
   }
    
}
```
### for-each Loop
used for printing arrays
```java
public class HelloWorld
{
   public static void main(String args[])
   {
     int[] arr = {2,4,5,7,8,0,3,5}
     for (int i : arr) {
     System.out.println(i);
   }
}
```
### do-while Loop
```java
public class HelloWorld
{
   public static void main(String args[])
   { 
        int i=1;
        do
        {
             System.out.println(i);
             i++;
        }while(i<=100);
   }
}
```

### Break statement

break keyword inside the loop is used to terminate the loop

```java
class HelloWorld
{
   public static void main(String args[])
   {
        int i;
        for(i=1;i<100;i++)
         {
              System.out.println(i);
              if(i==50)
	              break;
         }
   }
    
}
```

### Continue statement

continue keyword skips the rest of the current iteration of the loop and returns to the starting point of the loop

```java
class HelloWorld
{
   public static void main(String args[])
   {
        int i;
        for(i=1;i<100;i++)
         {
              System.out.println(i);
              if(i==50)
	              continue;
         }
   }
    
}
```

## Methods
### Declaration
Declaration of a method
```java
returnType methodName(parameters) {
//statements
}
```
### Calling a method
Calling a method
```java
methodName(arguments);
```

### Method Overloading

Method overloading means having multiple methods with the same name, but different parameters.

```java
class Calculate
{
  void sum (int x, int y)
  {
    System.out.println("Sum is: "+(a+b)) ;
  }
  void sum (float x, float y)
  {
    System.out.println("Sum is: "+(a+b));
  }
public static void main (String[] args)
{
   Calculate calc = new Calculate();
   calc.sum (5,4); //sum(int x, int y) is method is called.
   calc.sum (1.2f, 5.6f); //sum(float x, float y) is called.
}
}
```

### Recursion

Recursion is when a function calls a copy of itself to work on a minor problem. And the function that calls itself is known as the Recursive function.

```java
void recurse()
{
recurse();
}
```
## Strings

It is a collection of characters surrounded by double quotes.

### Creating String Variable

```java
String var_name = "Hello World";
```
### String Length

Returns the length of the string

```java
public class str
{
  public static void main(String args[])
  {
      String var_name = "Harry";
      System.out.println("The length of the string is: " + var_name.length());    
  }
}
```

### String Methods toUpperCase()
Convert the string into uppercase

```java
public class str
{
  public static void main(String args[])
  {
      String var_name = "Harry";
      System.out.println(var_name.toUpperCase());    
  }
}
```

### toLowerCase()
Convert the string into lowercase

```java
public class str
{
  public static void main(String args[])
  {
      String var_name = "Harry";
      System.out.println(var_name.toLowerCase());    
  }
}
```

### indexOf()
Returns the index of specified character from the string

```java
public class str
{
  public static void main(String args[])
  {
      String var_name = "Harry";
      System.out.println(var_name.indexOf("a"));    
  }
}
```

### concat()
Used to concatenate two strings

```java
public class str
{
  public static void main(String args[])
  {
    String var1 = "Harry";
    String var2 = "Bhai";
    System.out.println(var1.concat(var2));
  }
}
```

## Math Class

Math class allows you to perform mathematical operations.

### Methods max() method
It is used to find the greater number among the two

```java
public class Demo   
{  
  public static void main(String[] args)   
  {  
    // using the max() method of Math class  
    System.out.print("The maximum number is: " + Math.max(9,7));  
  }  
}  
```

### min() method
It is used to find the smaller number among the two

```java
public class Demo   
{  
  public static void main(String[] args)   
  {  
    // using the min() method of Math class  
    System.out.print("The maximum number is: " + Math.min(9,7));  
  }  
}  
```

### sqrt() method
It returns the square root of the supplied value

```java
public class Demo   
{  
  public static void main(String[] args)   
  {  
    // using the sqrt method of Math class  
    System.out.print("The maximum number is: " + Math.sqrt(144));  
  }  
}  
```

### random() method
It is used to generate random numbers

```java
Math.random(); //It will produce random number b/w 0.0 and 1.0
```

```java
public class Demo   
{  
  public static void main(String[] args)   
  {  
    // using the random() method of Math class  
    int random_num = (int)(Math.random() * 101); //Random num b/w 0 and 100
    System.out.println(random_num);
  }  
}  
```

## Exception Handling

An exception is an unusual condition that results in an interruption in the flow of the program.

### try-catch block

try statement allow you to define a block of code to be tested for errors. catch block is used to handle the exception.

```java
try {
// Statements
}
catch(Exception e) {
// Statements
}
finally {
// finally block always executes
}
```
