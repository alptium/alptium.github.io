# Нормализација базе података

Нормализација је поступак пројектовања логичке структуре базе података, где се настоји отклонити редуданса података без губитка информација.
Редунданса представља вишеструко меморисање исте информације у бази података.

Циљ нормализације је:

* контролисана редунданса података
* једноставно коришћење и мењање података(одржавање података)

Дефинисано је шест нормалних форми (НФ):

1. прва нормална форма (1NF),
2. друга нормална форма (2NF),
3. трећа нормална форма (3NF),
4. Boyce/Coddova normalna forma (BCNF),
5. четврта нормална форма (4NF),
6. пета нормална форма (5NF).

Што је ниво нормализације виши то је модел бољи – у њему има мање аномалија. У принципу важи да ако је модел у n нормалној форми, он је сигурно и у n-1 нормалној форми.

## Минималност кључа

Свођење кључа на минималан скуп атрибута представља прву етапу у нормализацији: Кључ је минималан скуп атрибута који дозвољавају да се сваки примерак (ентитета или везе) једнозначно идентификује.
Сви ентитети и везе имају бар један кључ а могу их имати и више. Осим за БојсКод нормалну форму (Boyce-Codd), нормализације се врши имајући у виду неки
задати кључ. 

## Прва нормална форма (1NF)

Ентитет или веза је у првој нормалној форми ако су сви његови атрибути елементарни (не могу се раставити).  Да би ентитет или веза били у 1NF треба декомпоновати сложене атрибуте – на
пример, увести атрибуте улица, поштанскиБрој, град, држава уместо сложеног атрибута адреса – или треба сложени атрибут заменити новим ентитетом, као у случају на слици:

![1nf](/github-slike/1NF.png)

## Друга нормална форма (2NF)

Ентитет или веза је у другој нормалној форми ако и само ако:

* је у првој нормалној форми, и
* ни један његов атрибути који није део кључа не зависи само од неког дела тог кључа.

Другим речима, атрибути треба да зависи од целог скупа атрибута који учествују у кључу. Према томе, ако је кључ сведен на само један атрибут или ако
садржи све атрибуте, ентитет или веза су обавезно у 2NF. Ентитет или веза могу да буду у другој нормалној форми у односу на један кандидат за кључ, а да не буду у
односу на неке друге кандидате.
Следећа слика приказује ентитет ПРОИЗВОД који описује производе које испоручују разни добављачи. Претпостављамо да једна добављач може да испоручи више
производа и да један производ може да испоручује више добављача. У том случају ни описПроизвода ни имеДобављача не могу сами да буду кључ ентитета ПРОИЗВОД.
Насупрот томе, кључ (описПроизвода, имеДобављача) јесте идентификатор ентитета ПРОИЗВОД. Међутим, атрибут адресаДобављача зависи само од дела кључа –
имеДобављача. Једно решење (неадекватно) је да се уведе нови атрибут идПроизвода који ће бити кључ, чиме ентитет прелази у 2NF. 

![2nf](/github-slike/2NF.png)

Овде претпостављамо да један добављач испоручује више производа и да више добављача може да испоручује један исти призвод.

## Трећа нормална форма (3NF)

Ентитет или веза је у трећој нормалној форми ако и само ако:
* је у другој нормалној форми, и
* ни један његов атрибути који није део кључа не зависи од неког скупа атрибута који нису у кључу.

Према томе, ако је ентитет или веза у другој нормалној форми и има само један атрибут који није у кључу он је обавезно у 3NF. Ентитет или веза могу да
буду у трећој нормалној форми у односу на један кандидат за кључ, а да не буду у односу на неке друге кандидате.
Током превођења у 3NF могу се открити и формулисати неки скривени ентитети:

![3nf](/github-slike/3NF.png)

У овом примеру атрибут адресаДобављача зависи од именаДобављача (заправо идДобављача).

## Бојс-Кодова нормална форма

Ентитет или веза је у Бојс-Кодовој нормалној форми ако и само ако постоји само таква међузависност атрибута у којој кључ одређује атрибут који није кључ.
Ентитет или веза који је у Бојс-Кодовој нормалној форми за један кандидат кључ је и за све остале кандидате. 

Погледајмо пример ентитета ДИПЛОМИРАНИ који моделира особу (име и презиме) која је стекла неку диплому (диплома) код неке образовне установе
(установа). Претпоставимо да није могућа ситуација у којој је једна особа стекла две исте дипломе, али да може да има више различитих диплома. Једна установа издаје
само једну врсту диплома, али исту диплому може да издаје више образованих установа. Ентитет ДИПЛОМИРАНИ има два кандидата за кључ:

* (име, презиме, установа)
* (име, презиме, диплома).

Ентитет ДИПЛОМИРАНИ није у 2NF у односу на кључ (име, презиме, установа) јер диплома зависи од установе. Насупрот томе, ентитет ДИПЛОМИРАНИ јесте у 3НФ у
односу на кључ (име, презиме, диплома) – зато што је у 2NF и има само један атрибут изван кључа. Па ипак, ентитет ДИПЛОМИРАНИ није у BCNF јер постоји зависност од атрибута
који није у кључу – диплома зависи од установе. Модел који је у Бојс-Кодовој нормалној форми се сматра да је довољно добар да може да се отпочне за имплементацијом базе. 

Пример превођења у Бојс-Кодову нормалну форму:

![bcnf](/github-slike/BCNF.png)

## Четврта и пета нормална форма

4NF se користи у случају када 3NF не може да заврши нормализацију; 4NF је значајна за ситуације где кључни податак има вишезначне зависности, које се могу до краја елиминисати тек свођењем на 5NF.

