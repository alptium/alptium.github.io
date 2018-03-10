## ELSE / IF FUNCTIONS <h2>


**Task:** Make a calculator which will have function that we can choose the operation. 

For needs of this task, we are introducing new commands, ELSE/ IF, which will be explained by following steps: 


**Example 1:** In this example, description of how function is working is simplified


```
package org.alptium.valentinacupac.samples.calculator;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		
		try(Scanner sc = new Scanner(System.in)) {

			String skyColor = "blue";
		
			if(skyColor == "blue")
			{
			System.out.println("The sky is blue, it's a nice day");
			}
			else if(skyColor == "grey")
			{
			System.out.println("The sky is gray, it's a cloudy day");
			}
			else if(skyColor == "red" )
			{
			System.out.println("The sky is red, it's a sunset");
		}
	}
}
```


**Task 2:** Display of a code in the program.


```
package org.alptium.valentinacupac.samples.calculator;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		
		try(Scanner sc = new Scanner(System.in)) {
			
			System.out.println("Enter your first number");
			int firstNumber = sc.nextInt();
			
			System.out.println("Choose your operation +, -, * ,/ ");
			String operation = sc.next();
			
			System.out.println("Enter your second number");
			int secondNumber = sc.nextInt();

			System.out.println("Now the system is calculating the result ...");
			int result = 0;
			
			if(operation.equals("+")) {
				result = firstNumber + secondNumber;
			} else if(operation.equals("-")) {
				result = firstNumber - secondNumber;
			} else if(operation.equals("*")) {
				result = firstNumber * secondNumber;		
			} else if(operation.equals("/")) {
				result = firstNumber / secondNumber;			
			}
			
			System.out.println("First number is: " + firstNumber);
			System.out.println("Second number is: " + secondNumber);
			System.out.println("The result is: " + result);
		}
	}
}
```

This code is applied to concrete task and it is shown below:


```
package calculator;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
	
		try(Scanner sc = new Scanner(System.in)) { 
	     
			System.out.println("Enter your first number"); 
		
			int a = sc.nextInt(); 
						   
			System.out.println("Chose your operation +, -, *, / "); 
		
			String op = sc.next(); 
		
			System.out.println("Enter your second number"); 
		
			int b = sc.nextInt(); 
		
			int c = 0;
 
			if(op.equals("+")) 
			{
				c = a + b;
			}
			else if(op.equals("-")) 
			{
				c = a - b;
			}
			else if(op.equals("*")) 
			{
				c = a * b;
			}
			else if(op.equals("/")) 
			{
				c = a / b;
			}
						   
			System.out.println("Now the system calculating the result..."); .
										   
			System.out.println("First number is: " + a);
			System.out.println("Second number is: " + b);
			System.out.println("The result is: " + c);
		}
	}
}
```

Now, let’s explain each line of code above which we’ve written:


```
package calculator;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
	
		try(Scanner sc = new Scanner(System.in)); -> Scanner is used for scanning and registering all methods, which we wrote and to switch to a program we make. 
	     
		System.out.println("Enter your first number"); -> Command for printing user the text within double quotes.
		
		int a = sc.nextInt(); -> *sc* is the “label” for scanner, and *nextInt* represents next INTEGER number which user enters.
						   
		System.out.println("Chose your operation +, -, *, / "); -> Command by which system prints user which operation to choose.
		
		String op = sc.next(); -> *STRING* *STRING* Represents array of characters which we’ve written in the previous line. From the other hand *sc.next* means that it chooses next operation of given. The result is array of characters.
		
		System.out.println("Enter your second number"); -> Command which prints user the txt within double quotes.
		
		int b = sc.nextInt(); -> The result is a number of a type INTEGER.
		
		int c = 0; -> -> Box with a name ‘c’, which is type INTEGER, has the default value 0, which means that it can have any value, bease it is not defined.
				
		if(op.equals("+")) -> If the operation is equal to + then  C = A + B
		{
			c = a + b;
		}
		else if(op.equals("-")) -> If the operation is equal to - then  C = A - B
		{
			c = a - b;
		}
		else if(op.equals("*")) -> If the operation is equal to * then  C = A * B
		{
			c = a * b;
		}
		else if(op.equals("/")) -> If the operation is equal to / then  C = A / B
		{
			c = a / b;
		}
						   
		System.out.println("Now the system calculating the result..."); ->  Line of code for printing command for calculating operations.
						
						   
		System.out.println("First number is: " + a);
		System.out.println("Second number is: " + b);
		System.out.println("The result is: " + c);

		These 3 lines show that program will print us: If the first number is A, if the second number is B, then the result is C.
		}
	}
}

 ======================================================================
