﻿## Базичне математичке операције (+, -, *, /) и изрази за коришћење базичних операција


Желимо да направимо програм, калкулатор који ће имати основне операције сабирања, одузимања, множења и дељења.
Прво желимо да програм изврши операцију сабирања целих бројева, затим одузимања, множења и дељења.
С обзиром да ћемо користити целе бројеве, варијаблу коју ћемо у програму писати је она која одређује целе бројеве, а то је *Integer*. 

*try(Scanner sc = new Scanner(System.in));* -> је синтакса који смо користили у овим задацима, а представља скенер који служи да сними и регирструје све методе које смо исписали и да их пребаци на програм који израђујемо.

* *Напомена:* У тренутку када у програм који пишемо унесемо Scanner синтаксу, програм ће од нас тражити да имплементирамо скенер, а то ћемо постићи ако задржимо курсор на синтакси где ће се након тога појавити прозор у оквиру којег треба изабрати опцију *import java.util.Scanner;*.

*import java.util.Scanner;* се након овога исписује на сам почетак програма, изнад *public class Main* што ће се видети у наредним задацима.


**Задатак 1:** Направити калкулатор који ће извршити операцију сабирања, притом ћемо користити енглеску реч 'sum' за ту операцију: 


```
package org.alptium.valentinacupac.samples.calculator;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		
		try(Scanner sc = new Scanner(System.in)) {  
	     
			System.out.println("Enter your first number"); 
		
			//Napraviti kutijicu tipa int,naziv a, i ubaciti vrednost iz citaca
			int a = sc.nextInt(); 
		   
			System.out.println("Enter your second number");
		
			//Napraviti kutijicu tipa int,naziv b, i ubaciti vrednost iz citaca
			int b = sc.nextInt(); 
		   
			System.out.println("Now the system calculate the sum");
		
			//Napraviti kutijicu tipa int, naziv c i ubaciti vrednost tako sto izracunamo vrednost iz a, PLUS vrednost iз b
		
			int c = a + b;

		   	System.out.println("First number is: " + a);
			System.out.println("Second number is: " + b);
			System.out.println("Sum is: " + c);
```


**Задатак 2:** Направити калкулатор који ће да изврши операцију одузимања и користићемо енглеску реч 'difference' за ту операцију: .


```
package org.alptium.valentinacupac.samples.calculator;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		
		try(Scanner sc = new Scanner(System.in)) {    
	     
			System.out.println("Enter your first number"); 
		
			//Napraviti kutijicu tipa int,naziv a, i ubaciti vrednost iz citaca
			int a = sc.nextInt(); 
		   
			System.out.println("Enter your second number");
		
			//Napraviti kutijicu tipa int,naziv b, i ubaciti vrednost iz citaca
			int b = sc.nextInt(); 
		   
			System.out.println("Now the system calculate the difference");
		
			//Napraviti kutijicu tipa int, naziv c i ubaciti vrednost tako sto izracunamo vrednost iz a, MINUS vrednost iz b
			int c = a - b;
   
			System.out.println("First number is: " + a);
			System.out.println("Second number is: " + b);
			System.out.println("Difference is: " + c);
```


**Задатак 3:** Направити калкулатор који ће извршити операцију множења и користићемо енглеску реч 'product' за ту операцију:


```
package org.alptium.valentinacupac.samples.calculator;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		
		try(Scanner sc = new Scanner(System.in)) {    
	     
			System.out.println("Enter your first number"); 
		
			//Napraviti kutijicu tipa int,naziv a, i ubaciti vrednost iz citaca
			int a = sc.nextInt(); 
		   
			System.out.println("Enter your second number");
		
			//Napraviti kutijicu tipa int,naziv b, i ubaciti vrednost iz citaca
			int b = sc.nextInt(); 
		   
			System.out.println("Now the system calculating the product...");
		
			//Napraviti kutijicu tipa int, naziv c i ubaciti vrednost tako sto izracunamo vrednost iz a, PUTA vrednost iz b
			int c = a * b;
   
			System.out.println("First number is: " + a);
			System.out.println("Second number is: " + b);
			System.out.println("Product is: " + c);
```


**Задатак 4:** Направити калкулатор који ће извршити операцију дељења и користићемо енглеску реч 'quotient' за ту операцију: .


```
package org.alptium.valentinacupac.samples.calculator;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		
		try(Scanner sc = new Scanner(System.in)) {      
	     
			System.out.println("Enter your first number"); 
		
			//Napraviti kutijicu tipa int,naziv a, i ubaciti vrednost iz citaca
			int a = sc.nextInt(); 
		   
			System.out.println("Enter your second number");
		
			//Napraviti kutijicu tipa int,naziv b, i ubaciti vrednost iz citaca
			int b = sc.nextInt(); 
		   
			System.out.println("Now the system calculating the quotient...");
		
			//Napraviti kutijicu tipa int, naziv c i ubaciti vrednost tako sto izracunamo vrednost iz a, PODELI vrednost iz b
			int c = a / b;

			System.out.println("First number is: " + a);
			System.out.println("Second number is: " + b);
			System.out.println("Quotient is: " + c);
```

===================================================================================
