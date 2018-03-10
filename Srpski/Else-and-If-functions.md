## ELSE / IF ФУНКЦИЈЕ <h2>


**Задатак:** Направити калкулатор који ће имати функцију такву да можемо изабрати операцију-

За потребе овог задатка уносимо нове команде, а то су ELSE / IF које ће бити објашњене у следећим корацима:


**Пример 1:** У овом примеру је упрошћен опис како функција функционише.


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


**Пример 2:** Приказ кода у програму.


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

Овај код примењен на конкретном задатку, изгледа овако: 


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

Следи објашњење за сваку линију предходног кода који смо написали:


```
package calculator;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
	
		try(Scanner sc = new Scanner(System.in)); -> СКЕНЕР СЛУЖИ ДА СНИМИ ИЛИ РЕГИСТРУЈЕ СВЕ МЕТОДЕ КОЈЕ СМО ИСПИСАЛИ И ДА ИХ ПРЕБАЦИ НА НАШ ПРОГРАМ. 
	     
		System.out.println("Enter your first number"); -> КОМАНДА ДА СИСТЕМ ШТАМПА КОРИСНИКУ СВЕ ОНО ШТО СМО ИСПИСАЛИ УНУТАР ЗАГРАДА.
		
		int a = sc.nextInt(); -> *sc* ЈЕ ОЗНАКА ЗА СКЕНЕР, А *nextInt* ОЗНАЧАВА СЛЕДЕЋИ ЦЕО БРОЈ КОЈИ КОРИСНИК КУЦА.
						   
		System.out.println("Chose your operation +, -, *, / "); -> КОМАНДА ДА СИСТЕМ ШТАМПА КОРИСНИКУ ОПЕРАЦИЈУ КОЈУ ИЗАБЕРЕ.
		
		String op = sc.next(); -> *STRING* ОЗНАЧАВА НИЗ КАРАКТЕРА КОЈИ СМО ИСПИСАЛИ У ПРЕДХОДНОЈ ЛИНИЈИ, ДОК *sc.next* ЗНАЧИ ДА БИРА СЛЕДЕЋУ ОПЕРАЦИЈУ ОД ПОНУЂЕНИХ. ЊЕГОВ РЕЗУЛТАТ ЈЕ НИЗ КАРАКТЕРА.
		
		System.out.println("Enter your second number"); -> КОМАНДА ДА СИСТЕМ ШТАМПА КОРИСНИКУ СВЕ ОНО ШТО СМО ИСПИСАЛИ УНУТАР ЗАГРАДА.
		
		int b = sc.nextInt(); -> ЊЕГОВ РЕЗУЛТАТ ЈЕ ЦЕО БРОЈ - INTEGER.
		
		int c = 0; -> КУТИЈИЦА ПОД ИМЕНОМ 'C', КОЈА ПРИПАДА ТИПУ ЦЕЛОГ БРОЈА, ИМА ВРЕДНОСТ 0 ШТО ЗНАЧИ ДА ЈЕ НЕОДРЕЂЕНА И МОЖЕ ИМАТИ БИЛО КОЈУ ВРЕДНОСТ.
				
		if(op.equals("+")) -> АКО ЈЕ ОПЕРАЦИЈА ЈЕДНАКА + ,ОНДА ЈЕ C = A + B
		{
			c = a + b;
		}
		else if(op.equals("-")) -> АКО ЈЕ ОПЕРАЦИЈА ЈЕДНАКА - ,ОНДА ЈЕ C = A - B
		{
			c = a - b;
		}
		else if(op.equals("*")) -> АКО ЈЕ ОПЕРАЦИЈА ЈЕДНАКА * ,ОНДА ЈЕ C = A * B
		{
			c = a * b;
		}
		else if(op.equals("/")) -> АКО ЈЕ ОПЕРАЦИЈА ЈЕДНАКА / ,ОНДА ЈЕ C = A / B
		{
			c = a / b;
		}
						   
		System.out.println("Now the system calculating the result..."); -> ЛИНИЈА КОЈА ЋЕ НАМ У ПРОГРАМУ ИШТАМПАТИ КОМАНДУ ЗА РАЧУНАЊЕ ОПЕРАЦИЈЕ.
						
						   
		System.out.println("First number is: " + a);
		System.out.println("Second number is: " + b);
		System.out.println("The result is: " + c);

		ОВЕ ТРИ ЛИНИЈЕ ГОВОРЕ ДА ЋЕ НАМ ПРОГРАМ ШТАМПАТИ: АКО ЈЕ ПРВИ БРОЈ А, ДРУГИ B, ОНДА ЋЕ РЕЗУЛТАТ БИТИ С.
		}
	}
}

 =================================================================================
