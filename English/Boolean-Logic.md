## Conditional statements - IF / ELSE and Boolean logic


This lection will demonstrate a practial base of programing. Every task within this program is based on a conditional statements IF / ELSE and comparative operations, respectively Boolean logic.

At the begining, we will demostrate operations which are used for forming the conditions in tasks.


                 **Comparison operators**


**<**	Less than 

**<=**	Les than or equal to

**>**	Greater than

**>=**	Greater than of equal to


                 **Equality operators**


**==**	equal to

**!=**	not equal to


                 **Boolean operations**


**&&**  "AND"

**||**  "OR"

**!**	"NOT"



The Task is to make a Banking program with the following conditions, which will be shown within types:


                double salary = 200.34;
		char gender = 'F';
		int age = 18;
		boolean isEmloyed = true;
		boolean isChild = true;



**Task 1:** Make a Banking program which determines condition that client has incomes up to a certain value and if so, credit can be approved.



```
package conditionals;

public class Main {

	public static void main(String[] args) {
		
		//sample: only salary is condition
		
		if (salary > 300.56) { // greater than
			System.out.println("Your loan has been approved");
		}else {
			System.out.println("Your loan has been declined / rejected");
		}
	}
}
```


This condition means that if users incomes are greater than 300.56 and (&&) if user is a female gender, program will print that credit has been allowed or that credit has been rejected. 

Considering that our user has incomes greater than 200.34 Eur (less than conditions) matching the female gender, and condition is that credit will be approved if incomes are greater than 300.56 and (&&) matching female gender, program will print that credit has been declined - > 'Your loan has been declined / rejected'. 


On this task, practical Boolean logic is noticeable, when on basic starting situation and condtition that are set, program determines  whether is something correct or incorrect, relatively if some action is possible or not.



**Task 2:** Make a Banking program wich determines condition that client has incomes to a certain value and (&&) condition that the client is a female gender.



```
package conditionals;

public class Main {

	public static void main(String[] args) {
		
		// Complex: must have both salary "AND" be female
		
		if(salary > 300.56 && gender == 'F') {
			System.out.println("Your loan has been approved");
		}else 
			System.out.println("Your loan has been declined / rejected");
		}
	}
}
```



**Task 3:**  Make a Banking program wich determines the condition that client has minimum incomes certain values or (||) 18 years.



```
package conditionals;

public class Main {

	public static void main(String[] args) {		
		
		// comlex: if either the person has minimun required salary, OR age is 18

		if(salary > 300.56 || age == 18) {
			System.out.println("Your loan has been approved");
		}else 
			System.out.println("Your loan has been declined / rejected");
		}
	}
}
```



This condition means that if client incomes are greater than 300.56 or (||) client has 18 years, program will print that credit is approved. Since our client has incomes of 200.34 Eur, which is less than conditions, but fulfills other conditions and that is that client has 18 years, program will print that credit is approved 'Your loan has been approved'. At || conditions, one of the values has to be true for fulfilling the condition.


**Task 4:** Make a Banking program wich determines the condition that client has minimum incomes of certain values or (||) 18 years of more than 18 years.



```
package conditionals;

public class Main {

	public static void main(String[] args) {		
		
		// comlex: if either the person has minimun required salary, OR age is greater than or equal 18
		
		if(salary > 300.56 || age >= 18) {
			System.out.println("Your loan has been approved");
		}else 
			System.out.println("Your loan has been declined / rejected");
		}
	}
}
```



This condition means that if users incomes are greater than 300.56 or (||) user has 18 years or more years, program will print that credit has been approved or that credit has been rejected. 
Considering that our user has incomes greater than 200.34 Eur, wich is less than conditions, but fulfills other condition and that is that user has 18 or more years, program will print that credit has been approved -> 'Your loan has been approved'.


**Task 5:** Make a Banking program wich determines the condition that client has minimum incomes of certain values or (||) has more than 18 years.



```
package conditionals;

public class Main {

	public static void main(String[] args) {
		
		// comlex: if either the person has minimun required salary, OR age is (strictly) greater than 18
		
		if(salary > 300.56 || age > 18) {
			System.out.println("Your loan has been approved");
		}else 
			System.out.println("Your loan has been declined / rejected");
		}
	}
}
```



This condition means that if users incomes are greater than 300.56 (||) or user has more than 18 years, program will print that credit has been approved or that credit has been rejected. 
Considering that our user has incomes greater than 200.34 Eur, wich is less than conditions, and it's not fulfilling the second condition wich is that has to have more than 18 years, program will print that credit has been rejected. 'Your loan has been declined / rejected'.


**Task 6:**  Make a Banking program wich determines a condition that client has minimum incomes of certain values and (&&) that client is employed.



```
package conditionals;

public class Main {

	public static void main(String[] args) {
		
		// comlex: if either the person has minimun required salary, AND person is emloyed
		
		if(salary > 300.56 && isEmployed) {
			System.out.println("Your loan has been approved");
		}else 
			System.out.println("Your loan has been declined / rejected");
		}
	}
}
```



This condition means that if incomes are greater than 300.56 and (&&) that user is employed, program will print credit is approved or credit is not approved. Considering that our user has income greater than 200.34 Eur, wich is less than conditions, and second condition is that the user is employed, program will print credit is not approved because both conditionals are not fulfilled. -> 'Your loan has been declined / rejected'.


**Task 7:** Make a Banking program wich determines conditions that client has minimum incomes of certain values and (&&) that the client is not a child.



```
package conditionals;

public class Main {

	public static void main(String[] args) {

		// comlex: if either the person has minimun required salary, AND person is "NOT" a child
		
		if(salary > 300.56 && !isChild) {
			System.out.println("Your loan has been approved");
		}else 
			System.out.println("Your loan has been declined / rejected");
		}
	}
}

```


This condition means that if clients incomes are greater than 300.56 and (&&) client is not a child, program will print that credit is approved or credit is not approved. Considering that our user has income greater than 200.34 Eur, wich is lass than conditionals, and fulfills the second one, wich is that the user is not a child, program will print that credit is not approved because both conditinals are not fulfilled. > 'Your loan has been declined / rejected'.



**Task 8:** In this task we setup the starting situation that the user has access to the Internet, has electronic device and has 10 years. However the conditionals of our program determine that profile on a social media can have a person wich has an access to the Internet, has electronic device and has less than 12 years.



```
package conditionals;

public class Main {

	public static void main(String[] args) {
	
		// account manager for Facebook, who makes accounts for people on Facebook
		
		// conditions - person must have acess to internet , must have electronic device, at least 12 years old
		// has internet access AND has electronic device, AND is at least 12

		boolean hasInternetAccess = true;
		boolean hasElectronicDevice = true;
		int age2 = 10;
		
		System.out.println();
		System.out.println();
		System.out.println();
		
		if(hasInternetAccess && hasElectronicDevice && age2 >= 12) {
			System.out.println("Your account has been created");
		}else 
			System.out.println("Your account has not been created");
		}
	}
}
```



Considering that user is fulfilling one of three conditions, program will determine that user can't open a profile on a social network.


========================================================================
