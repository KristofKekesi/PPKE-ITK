---
Óra neve: Bevezetés a programozásba I.
Előadó: Dr. Feldhoffer Gergely
Dátum:
---
# Sorozatok
Több hasonló adat érkezik a program számára.
### Jellemző műveletek:
- inicializálás
- következő elem olvasása
- sorozat végének felismerése / lekérdezése
### Ismert hosszú sorozat
- programba beleépített
- felhasználó által megadott
- érkező adatokból meghatározott
```
Változók:
	i, n: EGÉSZ,
	X : T

n := A sorozat hossza

i := 0
CIKLUS AMÍG i < n
	BE: X
	X feldolgozása
	i := i+1
CIKLUS_VÉGE
```
### Végjeles sorozat
- speciális érték / karakter jelöli a sorozat végét
- ==kötelező értékkészlet==
- értékkészlet alapján meghatározzuk ami nem eleme
```
Változók:
	X : T

BE: X
CIKLUS AMÍG X nem végjel
	X feldolgozása

	BE: X ** Előreolvasás

CIKLUS_VÉGE
```
# Fájlok
- névvel azonosítható adattároló
- ==A fájlok kezelése rendszertől, nyelvtől, kontextustól függ==
### Fájlok PlanG-ban
- bemeneti fájl (BEFÁJL): csak olvassuk
- kimeneti fájl (KIFÁJL): írunk
```
VÁLTOZÓK:
	a: BEFÁJL,
	n: EGÉSZ

MEGNYIT a "fájlnév"
BE a: n
LEZÁR a

KI: n
```
- Beolvassuk a fájlnév nevű fájlt, majd kiírjuk az első elemét
```
VÁLTOZÓK:
	a: BEFÁJL,
	n: EGÉSZ

MEGNYIT a "fájlnév"
BE a: n

CIKLUS AMÍG NEM VÉGE a
	KI: n, SV
	BE a: n
CIKLUS_VÉGE
LEZÁR a
```
- Beolvassuk a fájlnév nevű fájlt, majd kiírjuk az összes elemét ameddig vége nem lesz.