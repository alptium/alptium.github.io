# alptium.github.io
Alptium
Enter Enter test from Iva
ffodip;o]
edited from web
edited from desktop
# This is an <h1> tag
## This is an <h2> tag
###### This is an <h6> tag

* Item 1
* Item 2
  * Item 2a
  * Item 2b
  
  ![screenshot of github desktop](/images/github-desktop-01.jpg)




  # Uvod tekst <h1>


**УВОД**

Eclipse туторијал 
Еклипс је програмска развојна околина (integrated development environment (IDE) ) писана у Jaви, а може се користити за развој апликација у разним програмским језицима .
Jава је платформски независан програм што значи да када једном направите свој програм у Јави моћи ћете да га апликујете и активирате на многим другим и различитим платформама.
Овај туторијал ће вас научити како да развијете софтверски пројекат користећи Еклипс ИДЕ.

**Коме је туторијал намењен?**

Туторијал је намењен почетницима којима ће помоћи да разумеју основне функције Еклипс алата 

/*Овде ,с обзиром на то да ја са ове тачке не разумем како све то функционише ,оставила бих теби да додаш шта овај туторијал предвиђа, шта је то конкетно што ћемо научити и шта ћемо моћи на крају конкретно и урадити.*/

**Шта је то што вам је потребно ?**

За почетак је потребно  да имате инсталиране програме Јava JDK  и Eclipse.

**Упутства за инсталацију**
Инсталација Јава 9:
Google →  Download Java 9 Oracle →  Java SE Development Kit 9 –Downloads – Oracle →  klik na Acept Licence Agreement  →  zatim klik na : 

 ![Image](/slike/1a.png)

Изаберите да вам се сачува на вашем десктопу. Након тога када је преузимање завршено на вашем десктопу ће се појавити иконица Јава 9 еxe file → дупли клик на иконицу након чега ће се појавити :

 ![screenshot of github desktop](/slike/2a.png) 

клик на 'Yes’

/*овако или да на пример тебе снимим како ти инсталираш Јаву и Еклипс  па да то поставиш на сајту ,можда је тако лакше ,да имамо на српском језику.
Овде бих стала док ми не кажеш да ли да наставим на овај начин или правимо снимак,мени је свеједно,како ти кажеш */

**Како направити нови пројекат ?**

Креираћемо једноставан програм који ће нам на екрану приказати „Hello World!”
	Клик на File ,изаберемо New ,затим клик на Java project

 ![screenshot of github desktop](/slike/eklips3.png)

	Након ове команде појавиће се прозор у којем се уписује име новог пројекта (у овом случају  ‘Test project 2’ ) i →Finish

 ![screenshot of github desktop](/slike/eklips4.png)

У Еклипс програму се приказује фолдер који смо направили са именом који смо изабрали за пројекат.
     
![screenshot of github desktop](/slike/eklips10.png) 
 
![screenshot of github desktop](/slike/3a.png)

Следећи корак је :
Дупли клик на TestProject2  када нам се отварају нова поља у оквиру фолдера.
Напомена: ‘src’-source представља фајл у оквиру пројекта за складиштење програмских  кодова. 

Десни клик на ‘src’ → New → Class 
 
![screenshot of github desktop](/slike/eklips5.png)

Након овог корака отвара нам се прозор који именујемо са ‘Main’ и маркирамо поље под именом ‘public static void main’

 ![screenshot of github desktop](/slike/eklips11.png)

У овом трентку програм је задате команде генерисао и апликовао их на почетној (радној) страници Еклипс програма.
 
![screenshot of github desktop](/slike/eklips12.png)

Напомена: 
 **public class** = сваки фајл у Јава програму је означен са ‘class’ ,што значи да свака линија кода која се покреће треба бити унутар( ‘class’) класе. У овом случају ми смо ‘class’ или класу именовали као Main
 **public static void main (String[] args)** = ово говори програму да је то прва метода коју ће програм извршити. Програм је списак инструкција које ми желимо да се изврше.
У Јави свака апликација има стартну позицију (улазна тачка ),а то је метода која се означава као ‘main’. То значи да сваки Јава програм почиње од main методом.
	**public:** свако може приступити
	**static:** ово ако можеш ти објаснити шта означава
	**void:** ово ако можеш ти објаснити шта означава
	**main:** име методе

**Која метода штампа текст у Јава програму?** →System.out.println()

Следећи корак  →System .out.println (“Hello World!”); →File →Save →и корак за покретање кликом на Run main 

![screenshot of github desktop](/slike/eklipse9.png) 
 
Напомена: 
**System.out.println** → метода исписује линију текста на екрану ,у овом случају линија текста је ‘Hello World!”;
**;** → у Јави се свака команда мора завршити овим знаком.

![screenshot of github desktop](/slike/4a.png)
 
Рачунарска меморија се може објаснити на примеру кутијица :
 овде иде слика кутијица коју морам накнадно да направим

Да би обрађивали податке , потребно их је некако складиштити. Складиштење се врши у варијаблама или променљивим које у Јава језику  на почетку дефинишемо. Зато већина програмских језика има више типова информација које се уписују у варијабле. То су:

**Int** – Цели бројеви
**Double**– Децимални бројеви
**Char** - Карактери
**Boolean**– Тип променљиве која може да има само две вредности ( True , False )

Пример: задатак је креирати варијаблу типа Intiger ( int ) под именом ab која ће садржати вредност „14“. Команда која би ово извршила би изгледала овако.

![screenshot of github desktop](/slike/Int.JPG)

Пример: задатак је креирати варијаблу типа character ( char ) под именом jkl која ће садржати карактер  ‘a’.

![screenshot of github desktop](/slike/2.JPG)
 
 Напомена : карактери се увек записују са наводним знацима **‘** → ’карактер’

Пример: задатак је креирати варијаблу типа boolean (bool) под именом **yt** која ће садржати вредност True.
 
![screenshot of github desktop](/slike/5.JPG)

Напомена: Boolean тип може садржати само две вредности,или True или False.

Пример: задатак је креирати варијаблу типа dooble под именом **ujl** koja ће садржати децимални број 45,89.

![screenshot of github desktop](/slike/6.JPG) 

Напомена : децимални бројеви се у  Java језику  уместо зарезом одвајају тачком.
Ово су до сад били примери једноставних типова. Следећи тип је комплексан,састоји се од више карактера.

Пример комплексног типа String  под именом **jds** који садржи неколико карактера “Marija Marjanovic”

![screenshot of github desktop](/slike/7.JPG) 

Напомена: садржај овог типа се увек записују са дуплим наводним знацима **“**.
