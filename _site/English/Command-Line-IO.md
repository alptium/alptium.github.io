## Command line I/O (writing in System.out and reading from System.in) <h2> 


As we have learnt writing simple (primitive) and complex types of data, now, we can apply that knowledge in the following tasks.

**Task 1:**


In this task, apart from basic examples of types of variables, we will do as well operation add of two values.

In the first task, we choose program which will write values of Integer, with a name "ab". It is shown below:


**System.out.println("Value of ab: " + ab);** -> Program will print the text which is within double quotes + it will add the value “ab”. Between them, it will be space, as we put that within double quotes.

In the picture below, there are represented different examples.

*Note:* Two slashes which are shown in the picture are used for putting comments into a code. This means they are not part of a code, and program does not recognize it as lines of code. 


```
package org.alptium.valentinacupac.samples.calculator;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		
		//PRIMITIVE TYPES
		
		//Integer (int)

		int ab = 14;
		int lala = 150;
		int zebra = 234;
		int luk = 45;
		
		System.out.println("Value of ab: " + ab);
		
		//Character (char)

		char jkl = 'a' ;
		char gh = '8' ;
		char sfgs = '$' ;
		
		System.out.println("Value of sfgs: " + sfgs);
		
		//Boolean (bool)

		boolean yt = true;
		boolean lop = false;
		boolean df = true;
		
		System.out.println("Value of df: " + df);
		
		//Double

		double ujl = 45.89;
		double er = 786579.982;
		double vb = 0.06864;
		
		System.out.println("Value of er: " + er);
		
		//COMPLEX TYPES
		
		//String (tekst - niz karaktera)

		String jds = "Marija Marjanovic";
		String ywe = "Ulica 5, Beograd";
		String ulo = "Fly to the moon";
		
		
		System.out.println("Value of er: " + jds);
	}
}

```

After running the program, the program printed our commands as following:

Value of ab: 14

Value of sfgs: $

Value of df: true

Value of er: 786579.982

Value of er: Marija Marjanovic


**Task 2:**


In this task we want our program to print variables of type Integer.


 ```
package org.alptium.valentinacupac.samples.calculator;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		
		// Make a box of type int, with a name 'a' and put value 5.
		
		int a = 5;
		
		// Make a box of type int, with a name 'b' and put value 3.
		
		int b = 3;
		
		//Make a box of type int, with a name 'c' and put value as an addition of variables 'a' and 'b'.
		
		int c = a + b;
	}
}

```

 When we enter these values of variables into a line of writing program, it will looks like:


```
		System.out.println("a is: " + a);
		System.out.println("b is: " + b);
		System.out.println("c is: " + c);
```


After clicking button Run main, we’ve run the program. Program will print exactly what is within double quotes and more, it will add values (+a, +b, +c) with all spaces which we’ve put.


```
a is: 5
b is: 3
c is: 8
```
=====================================================================
