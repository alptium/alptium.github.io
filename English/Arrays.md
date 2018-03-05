## ARRAYS 


In this lesson, we will learn how to print the strings of some data in the easiest way. We will use a complex type of variable - Arrays.
Array is a collection of variables of the same type and in the examples will be shown the series for each type of variable separately.

When you need to keep a list of values, such as numbers, we can store them in a row instead of typing separate variables for each number as shown in the first example.


**Example 1:** Write a bank account of the user with the name, gender, account balance and data whether the user has taken a loan.

This would be the case for individual data writing, or writing separate variables for each String or character string:


```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {

		String person0 = "Valentina" ;
		String person1 = "Marija" ;
		String person2 = "Marko" ;
		String person3 = "Djordje";
		//etc.
	}
}
```

In memory, physically these arrays, that is, the data are located next to each other as shown in the picture and make one whole: 

PICTURE

The previous example of writing arrays is virtually the same as the next one to write, but in programming, we have a syntax for writing arrays that is more efficient in terms of program memory. In particular, in the following example, we will write a list of four people, and we will use a variable that denotes a string of characters, which is *String*:


**Example 2:** Write a array that will contain a list of people who have an account in the bank, using a type that indicates a string of characters, which is *String*:


```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {

//Array of strings (name of people who have bank account)

		String[] people = new String[4]; // array of string containing space for 4 strings
		people[0] = "Valentina";
		people[1] = "Marija";
		people[2] = "Marko";
		people[3] = "Djordje";
	}
}
```


*Note:* String[] people = new String[4]; - which would mean 'make a new series of characters and let their length be 4''

*Note:* String[] - these brackets means array of strings - array of characters or strings. Likewise, if we had a series of integers, the syntax would look like this -> int[] num;

In arrays, the elements of the string are sorted out and each has a specific and constant position, called an index. The index of the position of each element of the string is located within the square brackets.


**Example 3:** Write a set of data that determines the state of the account - *Balances*. For these data we will use the type of variable that determines decimal numbers, that is *Double*.


```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {

//Array of doubles (the bank accounts balance of those people)

		double[] balances = new double[4];
		balances[0] = 400.23;
		balances[1] = 800.24;
		balances[2] = 950.324;
		balances[3] = 28300.23;
	}
}
```


*Note:* The data positions within the index start at 0. This is the rule in the Java program, while in some other programs it starts from 1. 

*Note:* The names of variables in strings - 'Arrays' are written in the plural : balances, haveLoans, genders, accountIds... 


**Example 4:** Write down an array to show if customers have an open credit - *haveLoans*. For this operation, we will use a type of variable that has two values, true or false, and that is Boolean type.


```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {

//Array of boolean values ()

		boolean[] haveLoans = new boolean[4];
		haveLoans[0] = true;
		haveLoans[1] = true;
		haveLoans[2] = false;
		haveLoans[3] = true;
	}
}
```


*Note:* Names of Boolean variables, start with -have, -has, -is etc... 


**Example 5:** Write down the array by which we will present the account number. As far as integers are concerned, we will use type variables *Integer*.


```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {

//Array of integers

		int[] accountIds = new int[4];
		accountIds[0] = 10001;
		accountIds[1] = 10002;
		accountIds[2] = 10003;
		accountIds[3] = 10004;
	}
}
```


**Note:** Write down the array by which we will present a gender of the users. We will use a type of character variable, that is*Character*.


```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {

//Array of characters

		char[]genders = new char[4];
		genders[0] = 'F';
		genders[1] = 'F';
		genders[2] = 'M';
	}
}
```		

=======

