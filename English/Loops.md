## LOOPS - WHILE / FOR



In this lecture, we will learn how to change values in “memory boxes” by using loops.

Loops allow repetition of some statement or groups of statements. 

**Example:** This example will help us to understand how loops work: 

If we would change value which is inside the memory box, previous version which had been inside would be erased. This will be shown with following examples. It should be emphasized that it is possible to exist only one value inside memory box. 


```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {
		
		
		int lala2 = 5; //creating box in memory (informal) ---initialization and assignment
		lala2 = 7; //updating the value inside the box in memory (informal)--assignment - defining the value in the box
		lala2 = 100; //updating the value inside the box in memory (informal)--assignment - defining the value in the box		
		
		boolean mek = true;
		mek = false;
		mek = true;
		mek = true;
	}
}
```


If in a memory of a program we have an array of data, for example array of names in determined positions, as it is shown in example:


```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {

//Array of strings (name of people who have bank account)
				
		String[] people = new String[4]; // array of string containing space for 4 strings
		people[0] = "Iva";
		people[1] = "Marija";
		people[2] = "Marko";
		people[3] = "Djordje";
	}
}
```

...and we want program to write those values, then we need to introduce new syntax. That is a 'counter' which will facilitate the process of repeating some operation.  We will explain in the following example, where ‘i’ represents counter. This example will show us as well use of two types of variables -  Integer и Boolean.



```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {

//Array of strings (name of people who have bank account)
				
		String[] people = new String[4]; // array of string containing space for 4 strings
		people[0] = "Iva";
		people[1] = "Marija";
		people[2] = "Marko";
		people[3] = "Djordje";

		int i = 0; // this mean that the box is in memory, with name 'i'  and type integer , with a value equal to 0 
		
		while (i < 4) { // while 'i' less than  4, do all within { }
			
			System.out.println(people[i]); // write element from array 'people' in the position 'i'			
			i = i + 1; //EQUIVALENT TO: i++;
	}
}
```


This means that in the box 'i' value 0: **int i = 0;**. However, we put the condition that 'i' is less than  4: **while (i < 4)**. 

int = i + 1; this should be read from right to left, which means  result   **i + 1;** put into a box **'i'**


When we apply this operation in the system of loops (repeating), the program will behave like this:

1. If the value if box is 0, program is asking (checking the condition) if 0 < 4. As the statement is true, program will print value of people array with index 0. Previously, we determined that array of people with index number 0 has value 'Valentina', so that string will program print.

2. After this, there is another circle of loop. Previous value of box “i” will be erased and there is a new value equal to 1. **while (i < 4)**.

3. If the value of box is 1, program is asking (checking the condition) if 1 < 4. As the statement is true, program will print value of people array with index 1. Previously, we determined that array of people with index number 1 has value Marija, so that string will program print.

4. If the value of box is 2, program is asking (checking the condition) if 2 < 4. As the statement is true, program will print value of people array with index 2. Previously, we determined that array of people with index number 2 has value Marko, so that string will program print.

Program will repeat this operation until the following situation happens: 

5. If the value of box is 4, program is asking (checking the condition) if 4 < 4. As the statement is false, loops finishes here.
This means that program has printed names of people which we determine to be in the array up to index 4. 



We have one syntax which has the same, but it looks different: 


```
package conditionals;

import java.util.Date;

public class Main {

	public static void main(String[] args) {

//Array of strings (name of people who have bank account)
				
		String[] people = new String[4]; // array of string containing space for 4 strings
		people[0] = "Iva";
		people[1] = "Marija";
		people[2] = "Marko";
		people[3] = "Djordje";

		for (int j = 0; j < 4; j++) {
			System.out.println(people[j]); // write the element in position ј 
			j = j + 1;
		}
	}
}
```


This means:
- ј has value 0.
- Do commands within loop body..
- Icrease counter by 1 (ј++). 
- Do this until j < 4.
				
=======
