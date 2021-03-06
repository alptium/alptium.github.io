﻿## Покретање "Hello world" у Eclipsе програму


**Која метода штампа текст у Јава програму?** →System.out.println()


```
package helloworld;


public class Main {

	

	public static void main(String[] args) {
		
		System.out.println("Hello World");
	}
}
```


1. **File** → **Save** → и корак за покретање програма кликом на **Run main**. 

![screenshot of github desktop](/slike/eklipse9.png) 
 
Након тога у Eclipse програму у пољу испод кода који смо написали, програм ће штампати 'Hello World' као што је приказано на следећој слици:


![screenshot of github desktop](/slike1/24.JPG)

*Напомена:* 

**System.out.println** → је метода која исписује линију текста на екрану, у овом случају линија текста је 'Hello World'.

**;** → у Јави се свака команда мора завршити овим знаком.


## Креирање варијабли

 
Рачунарска меморија се може објаснити на примеру кутијица. Састоји се од кутијица које имају своје називе, а унутар сваке кутијице се налази неки садржај:


![screenshot of github desktop](/slike/tip1.png) 


![screenshot of github desktop](/slike/tip2.png) 


Да би обрађивали податке , потребно их је некако складиштити. Складиштење се врши у варијаблама или променљивим које у Јава језику на почетку дефинишемо. Зато већина програмских језика има више типова информација које се уписују у варијабле. Можемо их поделити на једноставне или примитивне типове и сложене или комплексне типове. 

Примери једноставних или примитивних типова су:

**Int** – **Intеger** = Тип променљиве која исписује целе бројеве.

**Double** – **Double precision floating number** = Тип променњиве која исписује децималне бројеве.

**Char** - **Character** = Тип променљиве који исписује појединачни карактер, знак или симбол.

**Bool** – **Boolean** = Тип променљиве која може да има само две вредности, тачно или нетачно, односно True или False.

Пример комплексног типа је:

**String** - Тип комплексне променљиве која се састоји из више карактера.


**Пример:** задатак је креирати варијаблу типа *intiger ( int )* под именом **ab** која ће садржати вредност „14“. Команда која би ово извршила би изгледала овако.

```
                int ab = 14;
		int lala = 150;
		int zebra = 234;
		int luk = 45;
```

**Пример:** задатак је креирати варијаблу типа *character ( char )* под именом **jkl** која ће садржати карактер  ‘a’.

```
                char jkl = 'a' ;
		char gh = '8' ;
		char sfgs = '$' ;
```
 
*Напомена:* карактери се увек записују са наводним знацима **‘** → ’карактер’

**Пример:** задатак је креирати варијаблу типа *boolean (bool)* под именом **yt** која ће садржати вредност True.
 
```
                boolean yt = true;
		boolean lop = false;
		boolean df = true;
```

*Напомена:* Boolean тип може садржати само две вредности,или True или False.

**Пример:** задатак је креирати варијаблу типа *double* под именом **ujl** koja ће садржати децимални број 45,89.

```
                double ujl = 45.89;
		double er = 786579.982;
		double vb = 0.06864;
``` 

*Напомена:* децимални бројеви се у  Java језику  уместо зарезом одвајају тачком.


Ово су до сад били примери једноставних типова. Следећи тип је комплексан, састоји се од више карактера.

**Пример** комплексни тип варијабле *String*  под именом **jds** који садржи више карактера “Marija Marjanovic”

```
                String jds = "Marija Marjanovic";
		String ywe = "Ulica 5, Beograd";
		String ulo = "Fly to the moon";
``` 

*Напомена:* садржај овог типа се увек записују са дуплим наводним знацима **“**.

=================================================================================
