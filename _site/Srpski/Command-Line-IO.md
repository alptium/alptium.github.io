## Командна линија I/O (писање у **System.out** и читање из **System.in**) <h2> 


Када смо научили писање једноставних(примитивних) и сложених типова, сада ћемо их применити у следећим задацима.

**Задатак 1:**


У овом задатку ћемо поред основних примера варијабли, односно типова, применити могућност сабирања две вредности од оних које су нам понуђене.

У првом примеру смо изабрали да нам програм испише вредности Integer, односно целог броја под називом "ab". И то ће изгледати овако:

**System.out.println("Value of ab: " + ab);** -> оно што је у загради унутар наводника програм исписује, а затим додаје вредност ab, притом ће програм поштовати и сваки размак који смо ставили унутар заграда.

На слици испод су приказани примери.

*Напомена:* Две косе црте које су приказане на слици служе за писање коментара, то значи да нису у склопу кода и да их програм као такве и региструје. 


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

Овако је програм исписао наше команде:

Value of ab: 14

Value of sfgs: $

Value of df: true

Value of er: 786579.982

Value of er: Marija Marjanovic


**Задатак 2:**


У овом задатку желимо да нам програм испише вредности варијабли типа Integer, односно целих бројева.


 ```
package org.alptium.valentinacupac.samples.calculator;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		
		// Napraviti kutijicu tipa int, naziv 'a' i ubaciti vrednost 5.
		
		int a = 5;
		
		//Napraviti kutijicu tipa int, naziv 'b' i ubaciti vrednost 3.
		
		int b = 3;
		
		//Napraviti kutijicu tipa int, naziv 'c' i ubaciti vrednost tako sto izracunamo vrednost iz 'a' PLUS vrednost iz 'b'.
		
		int c = a + b;
	}
}

```

 Када ове вредности и команде унесемо у линију за писање програма, то ће изгледати овако:


```
		System.out.println("a is: " + a);
		System.out.println("b is: " + b);
		System.out.println("c is: " + c);
```


Када кликнемо на **Run main** и тако покренемо програм, програм ће штампати тачно оно што се налази између знакова наводника и на то се додаје вредност ( + b и + c), наравно испоштоваће и размаке.


```
a is: 5
b is: 3
c is: 8
```
===========================================================================
