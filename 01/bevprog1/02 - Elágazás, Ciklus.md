---
Óra neve: Bevezetés a programozásba I.
Előadó: Dr. Feldhoffer Gergely
Dátum:
---
## Plang szintaktika:
- PROGRAM
- PROGRAM_VÉGE
## Program konstrukciók
### Szekvencia
több feladat elvégzése
### Elágazás
- Csak adott sorok lefuttatása
```Plang
HA <feltétel> AKKOR
	<futtatandó sorok ha igaz>
KÜLÖNBEN
	<futtatandó sorok ha hamsi>
HA_VÉGE
```

> [!warning] Fontos
> PlanG-ban nincs `else if`, ezért ezt a nyelvi funkciót egymásba ágyazott elágazásokkal tudjuk replikálni.
### Ciklus
- Benne lévő sorok ismétlése ameddig a feltétel igaz
- Manuálisan kell a feltételt igaznak tartani
```Plang
CIKLUS AMÍG <ciklusfeltétel>
	<ciklusmag>
CIKLUS_VÉGE
```
- egy lefutása a ciklusnak az __iteráció__
- minden iteráció után újra kiértékelődik a ciklus feltétel
#### Elöltesztelő ciklus:
A ciklus feltételt a ciklusmag előtt értékeljük ki.
```Plang
CIKLUS AMÍG <ciklusfeltétel>
	<ciklusmag>
CIKLUS_VÉGE
```
#### Hátultesztelő ciklus:
A ciklus feltételt a ciklusmag után értékeljük ki.
```Plang
CIKLUS
	<ciklusmag>
AMÍG <ciklusfeltétel>
```

> [!example]- Példa for ciklusra
> ```Plang
> i := 0
> CIKLUS AMÍG i < 10
>	** ciklusmag
>	i := i + 1
>CIKLUS_VÉGE
>```
#### Végtelen ciklus:
- Ha a ciklusfeltétel mindig igaz, vagy
- ha a ciklusfeltétel független a ciklusmagtól

> [!info]
> A végtelen ciklusok PlanG-ban alapjáraton 10.000 iterációig futnak le, ez maximum 100.000 iterációra húzható fel.
## Specifikáció
Leírás hogy miket kérünk be, miket adunk vissza. Mit milyen értékekkor, mit csinál a kódunk.
```Plang
** Egy komment a Plang-ban
```
###### Például:
Cél: Adjuk meg egy valós szám gyökét
Mi van ha a szám negatív?
- a program futásidejű hibával leáll
- a program nem ad semmilyen eredményt
- a program kiírja hogy érvénytelen adat
### Előfeltétel:
Milyen bemeneteket kell minden esetben kezelnie a programnak
**Például**:
- BE: a: nem negatív valós szám
- KI: b: nem negatív valós szám, ahol $b\cdot b=a$
### Utófeltétel:
- Amit visszaadunk mi alapján van.