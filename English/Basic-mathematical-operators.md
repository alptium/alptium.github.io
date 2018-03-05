## Basic mathematical operations (+, -, /, *) and mathematical expressions for using basic operations 


We want to make a program, calculator, which will have the basic operations – addition, subtraction, division and multiplication.
Firstly, we want program to do addition of Integer numbers, then subtraction, division and multiplication. 
It will be used *Integer* type of variables.

*try(Scanner sc = new Scanner(System.in));* ->  is the syntax which we’ve used in these tasks and represents scanner. It is used to scan and register all methods, which we wrote and to switch to a program we make.

* Note: * At the moment we enter the Scanner syntax in the program, the program will ask us to implement the scanner, and this will be achieved by holding the cursor to the syntax where a window will appear in which you want to select the * import java option. util.Scanner;*.

*import java.util.Scanner;* after this it is printed at the very beginning of the program, above * public class Main * which will be shown in the following tasks.


**Task 1:** Make a calculator which will do addition of two variables. For this operation we will use the word “sum” for this operation: 


```
package org.alptium.valentinacupac.samples.calculator;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		
		try(Scanner sc = new Scanner(System.in)) {  
	     
			System.out.println("Enter your first number"); 
		
			//Make a box of type int, with a name 'a' and put value from reader
			int a = sc.nextInt(); 
		   
			System.out.println("Enter your second number");
		
			//Make a box of type int, with a name 'b' and put value from reader
			int b = sc.nextInt(); 
		   
			System.out.println("Now the system calculate the sum");
		
			//Make a box of type int, with a name 'a' and put value as a result of addition of values a and b (a+b)	
		
			int c = a + b;
   
			System.out.println("First number is: " + a);
			System.out.println("Second number is: " + b);
			System.out.println("Sum is: " + c);
```


**Task 2:** Make a calculator which will do subtraction of two variables. For this operation we will use the word 'difference' for this operation: .


```
package org.alptium.valentinacupac.samples.calculator;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		
		try(Scanner sc = new Scanner(System.in)) {    
	     
			System.out.println("Enter your first number"); 
		
			//Make a box of type int, with a name 'a' and put value from reader
			int a = sc.nextInt(); 
		   
			System.out.println("Enter your second number");
		
			//Make a box of type int, with a name 'b' and put value from reader
			int b = sc.nextInt(); 
		   
			System.out.println("Now the system calculate the difference");
		
			//Make a box of type int, with a name 'a' and put value as a result of subtraction of values a and b (a-b)	
			int c = a - b;
			
			System.out.println("First number is: " + a);
			System.out.println("Second number is: " + b);
			System.out.println("Difference is: " + c);
```


**Task 3:** Make a calculator which will do multiplication of two variables. For this operation we will use the word 'product': 


```
package org.alptium.valentinacupac.samples.calculator;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		
		try(Scanner sc = new Scanner(System.in)) {    
	     
			System.out.println("Enter your first number"); 
		
			//Make a box of type int, with a name 'a' and put value from reader		
			int a = sc.nextInt(); 
		   
			System.out.println("Enter your second number");
		
			//Make a box of type int, with a name 'b' and put value from reader		
			int b = sc.nextInt(); 
		   
			System.out.println("Now the system calculating the product...");
		
			//Make a box of type int, with a name 'a' and put value as a result of multiplication of values a and b (a*b)	
			int c = a * b;
   
			System.out.println("First number is: " + a);
			System.out.println("Second number is: " + b);
			System.out.println("Product is: " + c);
```


**Task 4:** Make a calculator which will do division of two variables. For this operation we will use the word 'quotient':


```
package org.alptium.valentinacupac.samples.calculator;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		
		try(Scanner sc = new Scanner(System.in)) {      
	     
			System.out.println("Enter your first number"); 
		
			//Make a box of type int, with a name 'a' and put value from reader
			int a = sc.nextInt(); 
		   
			System.out.println("Enter your second number");
		
			//Make a box of type int, with a name 'b' and put value from reader
			int b = sc.nextInt(); 
		   
			System.out.println("Now the system calculating the quotient...");
		
			//Make a box of type int, with a name 'a' and put value as a result of division of values a and b (a/b)
			int c = a / b;
   
			System.out.println("First number is: " + a);
			System.out.println("Second number is: " + b);
			System.out.println("Quotient is: " + c);
```

===============================================================================
