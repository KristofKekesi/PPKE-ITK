# 1. ZH gyakorlás
## PlanG pót zárthelyi feladatok
### 1.) Milyen típusúak lehetnek az alábbi változók? Sorolj föl minél többet! (3 pont)
a := |t| = 10 ÉS RND 1000 MOD x > 0
Válasz: a: SZÖVEG, TÖMB; x: EGÉSZ, VALÓS
### 2.) Írj végtelen ciklust! (3 pont)
```Plang
CIKLUS AMÍG IGAZ
	ciklusmag
CIKLUS_VÉGE
```
### 3.) írj kifejezést! (3 pont)
SZAM szoveg\[\|szoveg\| - 1\]
### 4.) Mit ír ki a kimenetre a kód? (3 pont)
```Plang
PROGRAM bp1ppzh_01
	VÁLTOZÓK:
		i: EGÉSZ
	  i := 30

  CIKLUS AMÍG i > 12
    KI: i + 7, " "
    i := i - 3
	CIKLUS_VÉGE

  KI: i MOD 5
PROGRAM_VÉGE
```
Kimenet: 37 34 31 28 25 22 19 2
### 5.) Melyik programozási tételt használnád az alábbi feladat megoldására? Miért? (3 pont)
Egy tetszőleges szövegről add meg, hány számjegy, hány nagybetű és hány kisbetű van benne!
Válasz: Számlálás tételét, mert meg kell számolnunk egy ciklussal végigmenvén egy szövegen hogy az adott karakter megfelel e a feltételeknek, ha igen az adott számlálót a három közül növeljük eggyel.
### 6.) Melyik programozási tételt használnád az alábbi feladat megoldására? Miért? (3 pont)  
Egy egész számokból álló számsorból add meg a legnagyobbat!
Válasz: Maximumkeresés tételét, mert a legnagyobb értéket keressük egy adott sorozaton belül. Ciklussal végigmegyünk a sorozaton, az első betudjuk a legnagyobbnak, majd ha a soron következő értékek közül valamelyik nagyobb értékkel rendelkezik akkor a változót amiben a maximum értéket tároljuk módosítjuk.
### 7.) Mit ad meg az alábbi kifejezés? Rajzold fel a szintaxisfát is! (6 pont)
x:=(67 + (t MOD 4)^2) * RND 45
### 8.) Javítsd ki a kódot úgy, hogy a hárommal osztható számokat írja ki 100 és n között! Tabuláld helyesen! (6 pont)  
(specifikáció: BE: egész szám (n), n>100, KI: hárommal osztható számok 100 és n között)
```Plang
program bp1ppzh_02
változók:

n, x: logikai, a: egész
ha 3 MOD x := 6 akkor
be: i
i := 1000

ciklus amíg i > n
ki: egész, " "
i := 100-1
program_vége
ciklus_vége
```
Javított:
```Plang
PROGRAM bp1ppzh_02
VÁLTOZÓK:
	n, i, a: egész

BE n
i := 100
CIKLUS AMÍG i > n
	HA i MOD 3 = 0 akkor
		KI: i, " "
	HA_VÉGE
	i := i + 1
CIKLUS_VÉGE

PROGRAM_VÉGE
```
### 9.) Add meg egy tetszőleges szövegnek minden szavát külön-külön! (8 pont)
```Plang
PROGRAM p

VÁLTOZÓK:
	szoveg: SZÖVEG,
	i: EGÉSZ,
	elozoWhiteSpace: LOGIKAI

BE: szoveg
i := 0
elozoWhiteSpace: HAMIS
CIKLUS AMÍG i < |szoveg|
	HA BETŰ szoveg[i] VAGY SZÁM szoveg[i] AKKOR
		KI: szoveg[i]
		elozoWhiteSpace := HAMIS
	KÜLÖNBEN:
		HA NEM elozoWhiteSpace AKKOR
			KI: ", "
		HA_VÉGE
		elozoWhiteSpace := IGAZ
	HA_VÉGE
	i := i + 1
CIKLUS_VÉGE

PROGRAM_VÉGE
```
### 10.) Egy tetszőleges szövegről add meg, hány mondat található benne! (10 pont)
Mondatnak tekintünk minden olyan sort, ami nagybetűvel kezdődik, és ponttal, felkiáltójellel vagy kérdőjellel végződik.
```Plang
PROGRAM p

VÁLTOZÓK:
	szoveg: SZÖVEG,
	n, i, szamlalo: EGÉSZ

BE: n
i := 0
szamlalo := 0
CIKLUS AMÍG i < n
	BE: szoveg
	HA NAGY szoveg[0] VAGY SZÁM szoveg[0] AKKOR
		HA szoveg[|szoveg|-1] = '.' VAGY szoveg[|szoveg|-1] = '!' VAGY szoveg[|szoveg|-1] = '?' AKKOR
			szamlalo := szamlalo + 1
		HA_VÉGE
	HA_VÉGE
	i := i + 1
CIKLUS_VÉGE

KI: szamlalo

PROGRAM_VÉGE
```
### 11.) Fésülj össze két monoton növekvő sorozatot fájlból! (12 pont)
specifikáció: BE: két fájl, bennük növekvő sorrendben számok, KI: a két növekvő sorozat összefésülve (tehát növekvő sorrendben)
```Plang
PROGRAM p

VÁLTOZÓK:
	af, bf: BEFÁJL,
	a, b: EGÉSZ

MEGNYIT af: "a"
MEGNYIT bf: "b"

BE af: a
BE bf: b

CIKLUS AMÍG NEM VÉGE af VAGY NEM VÉGE bf
	HA a < b AKKOR
		KI: a
		BE af: a
	KÜLÖNBEN
		KI: b
		BE bf: b
	HA_VÉGE
CIKLUS_VÉGE

CIKLUS AMÍG NEM VÉGE af
	KI: a
	BE af: a
CIKLUS_VÉGE

CIKLUS AMÍG NEM VÉGE bf
	KI: b
	BE bf: b
CIKLUS_VÉGE

PROGRAM_VÉGE
```
## Kódjavítás
Az alábbi PlanG kódot javítsd, illetve egészítsd ki úgy, hogy a megadott specifikációnak eleget tegyen:
### a) (6 pont)
bemenet: valós számok 10 hosszú (s) sorozata  
kimenet: a -10 és 10 közötti nem nulla számok száma (c)
```Plang
    PROGRAM intervallum
       VÁLTOZÓK:

         s : VALÓS[10],
         i, c : EGÉSZ

       i := 1
       CIKLUS AMÍG i < 10

         BE : s[i]
       CIKLUS_VÉGE
       CIKLUS

         i := i+1
         HA ( | s[i] | > 0 ) AKKOR c = 1
         AMÍG i < 10

HA_VÉGE

       KI: c
    PROGRAM_VÉGE
```
Válasz:
```Plang
PROGRAM intervallum
VÁLTOZÓK:
	s: VALÓS[10],
	i, c: EGÉSZ

i := 0
CIKLUS AMÍG i < |s|
	BE: s[i]
	HA s[i] > -10 ÉS NEM (s[i] = 0) ÉS s[i] < 10 AKKOR
		c := c + 1
	HA_VÉGE
CIKLUS_VÉGE
```