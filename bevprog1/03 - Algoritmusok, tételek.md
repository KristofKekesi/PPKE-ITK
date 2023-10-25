---
Óra neve: Bevezetés a programozásba I.
Előadó: Dr. Feldhoffer Gergely
Dátum:
---
# Algoritmus
Az algoritmus egy megengedett lépésekből álló módszer, utasítássorozat, részletes útmutatás, recept, amely alkalmas arra, hogy valamilyen felmerülő problémára megoldást adjon.

- Általánosan van megfogalmazva, így több nyelven is leírható

# Összegzés tétele
Mennyi a sorozatban lévő számok összege?
```
VÁLTOZÓK:
	összeg, a: T

	összeg := 0
	CIKLUS AMÍG <nincs vége a sorozatnak>
		a := <következő elem> **lehet bekérdezés is
		összeg := összeg + a
	CIKLUS_VÉGE
```
# Számlálás tétele
Hány x elem van a sorozatban?
```
VÁLTOZÓK:
	a: T,
	számláló: EGÉSZ

CIKLUS AMÍG <nincs vége a sorozatnak>
	a := <következő elem>
	HA <feltétel a-ra> AKKOR
		számláló := számláló + 1
	HA_VÉGE
CIKLUS_VÉGE
```
# Lineáris keresés tétele
Melyik az első eleme a sorozatnak ami teljesít egy feltételt?
```
VÁLTOZÓK:
	a: T,
	van: LOGIKAI,
	i, hol: EGÉSZ

van := HAMIS
hol := 0
i := 0
CIKLUS AMÍG <nincs vége a sorozatnak> ÉS NEM VAN
	a := <következő elem>
	HA <feltétel a-ra> AKKOR
		hol := i
	HA_VÉGE
	i := i + 1
CIKLUS_VÉGE
```
# Maximum keresés tétele
Melyik a sorozat legnagyobb eleme?
```
VÁLTOZÓK:
	a, max: T,
	i, hol: EGÉSZ

a := <első elem>

i := 0
hol := 0
max := a

CIKLUS AMÍG <nincs vége a sorozatnak>
	a := <következő elem>
	HA a > max AKKOR
		hol := i
		max := 0
	HA_VÉGE
	i := i + 1
CIKLUS_VÉGE
```