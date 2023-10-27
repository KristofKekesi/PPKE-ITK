---
Óra neve: Bevezetés a programozásba I.
Előadó: Dr. Feldhoffer Gergely
Dátum:
---
## Plang szintaktika:
- PROGRAM
- PROGRAM_VÉGE

# Program konstrukciók
## Szekvencia
több feladat elvégzése

## Elágazás
- Csak adott sorok lefuttatása

```
HA <feltétel> AKKOR
	<futtatandó sorok ha igaz>
KÜLÖNBEN
	<futtatandó sorok ha hamsi>
HA_VÉGE
```

- ==Nincs else if==: ezért egymásba ágyazzuk a `KÜLÖNBEN`-eket

## Specifikáció
Leírás hogy miket kérünk be, miket adunk vissza. Mit milyen értékekkor.

```
** Egy komment a Plang-ban
```

#### Pl:
Cél: Adjuk meg egy valós szám gyökét
Mi van ha a szám negatív?
- a program futásidejű hibával leáll
- a program nem ad semmilyen eredményt
- a program kiírja hogy érvénytelen adat

### Előfeltétel:
Milyen bemeneteket kell minden esetben kezelnie a programnak

Pl:
- BE: a: nem negatív valós szám
- KI: b: nem negatív valós szám, ahol $b\cdot b=a$
### Utófeltétel:

## Ciklusok
- Benne lévő sorok ismétlése ameddig a feltétel igaz
- Manuálisan kell a feltételt igaznak tartani

```
CIKLUS AMÍG <ciklusfeltétel>
	<ciklusmag>
CIKLUS_VÉGE
```

- egy lefutása a ciklusnak az __iteráció__
- minden iteráció után újra kiértékelődik a ciklus feltétel

### Elöltesztelő ciklus:
A ciklus feltételt a ciklusmag előtt értékeljük ki.

```
CIKLUS AMÍG <ciklusfeltétel>
	<ciklusmag>
CIKLUS_VÉGE
```
### Hátultesztelő ciklus:
A ciklus feltételt a ciklusmag után értékeljük ki.

```
CIKLUS
	<ciklusmag>
AMÍG <ciklusfeltétel>
```


#### Példa for ciklusra
```
i := 0
CIKLUS AMÍG i < 10
	<ciklusmag>
	i := i + 1
CIKLUS_VÉGE
```

### Végtelen ciklus:
A ciklusfeltétel mindig igaz. Plangban csak 10.000-ig fut.