# 1. Kifejezések
## 1.5b.plang
> Döntsd el, hogy bármelyik osztója-e a másiknak.
```PlanG
PROGRAM a
VÁLTOZÓK:
	a, b: EGÉSZ

BE: a, b
KI: b MOD a = 0 VAGY a MOD b = 0

PROGRAM_VÉGE
```
## 1.8a.plang
> Add meg egy számtani sorozat első két elemének ismeretében a harmadik elemét.
```PlanG
PROGRAM a
VÁLTOZÓK:
	a, b, c: VALÓS

BE: b, c
a := c - b

KI: c + a

PROGRAM_VÉGE
```
## 1.8b.plang
> Add meg az N-edik elemét.
```PlanG
PROGRAM a
VÁLTOZÓK:
	a, b, c, n: VALÓS

BE: b, c, n
a := c - b

KI: b + (n - 1) * a  

PROGRAM_VÉGE
```
## 1.8c.plang
> Mértani sorozatra is add meg az N-edik elemet.
```PlanG
PROGRAM a
VÁLTOZÓK:
	q, b, c, n: VALÓS

BE: b, c, n
q := c / b

KI: q ^ (n - 1) * b

PROGRAM_VÉGE
```
## 1.11a.plang
> Add meg egy koordinátákkal adott pont távolságát az origótól.
```PlanG
PROGRAM a
VÁLTOZÓK:
	x, y: VALÓS

BE: x, y
KI: (((0 - x)^2)+((0 - y)^2))^0.5

PROGRAM_VÉGE
```
## 1.11b.plang
> Két tetszőleges, koordinátáival adott pont távolságát add meg.
```PlanG
PROGRAM a
VÁLTOZÓK:
	x1, y1, x2, y2: VALÓS

BE: x1, y1, x2, y2
KI: (((x1 - x2)^2)+((y1 - y2)^2))^0.5

PROGRAM_VÉGE
```
## 1.15.plang
> Döntsd el egy szövegről, hogy nagybetűvel kezdődik e.
```PlanG
PROGRAM a
VÁLTOZÓK:
	a: SZÖVEG

BE: a
KI: a[0] = (NAGY a[0]) ÉS (NEM (SZÁM a[0]))

PROGRAM_VÉGE
```
## 1.16.plang
> Döntsd el egy szövegről, hogy számjegyre végződik-e.
```PlanG
PROGRAM a
VÁLTOZÓK:
	a: SZÖVEG

BE: a
KI: SZÁM a[|a| - 1]

PROGRAM_VÉGE
```
## 1.17a.plang
> Döntsd el egy szövegről, hogy ugyanazzal a karekterrel kezdődik-e, mint amivel végződik.
```PlanG
PROGRAM a
VÁLTOZÓK:
	a: SZÖVEG

BE: a
KI: a[0] = a[|a| - 1]

PROGRAM_VÉGE
```
## 1.17b.plang
> Azt is fogadd el egyezésnek, ha az egyik kisbetű, a másik nagybetű (pl. nagy A-val kezdődik, kis a-ra végződik).
```PlanG
PROGRAM a
VÁLTOZÓK:
	a: SZÖVEG

BE:a
KI: NAGY a[0] = NAGY a[|a| - 1]

PROGRAM_VÉGE
```
## 1.18.plang
> Döntsd el két szövegről, hogy megegyezik-e az első öt karakterük.
```PlanG
PROGRAM a
VÁLTOZÓK:
	a, b: SZÖVEG

BE: a, b
KI: |a| > 4 ÉS |b| > 4 ÉS (a[0:5] = b[0:5])

PROGRAM_VÉGE
```
## 1.19a.plang
> Add meg egy tetszőleges szöveg első szavát.
```PlanG
PROGRAM a
VÁLTOZÓK:
	a: SZÖVEG,
	n: EGÉSZ

BE: a
n := a @ ' '
KI: a[0:n]

PROGRAM_VÉGE
```
## 1.21a.plang
> Két tetszőleges szövegről döntsd el, hogy az első megtalálható-e a másodikban.
```PlanG
PROGRAM a
VÁLTOZÓK:
	a, b: SZÖVEG

BE: a, b
KI: NEM (b @ a = |b|)  

PROGRAM_VÉGE
```
## 1.21b.plang
> Két tetszőleges szövegről döntsd el, hogy valamelyik megtalálható-e a másikban.
```PlanG
PROGRAM a
VÁLTOZÓK:
	a, b: SZÖVEG

BE: a, b
KI: (NEM (a @ b = |a|)) VAGY (NEM (b @ a = |b|))

PROGRAM_VÉGE
```
## 1.21c.plang
> Egy szövegből töröld ki egy másik szöveg első előfordulását.
```PlanG
PROGRAM a
VÁLTOZÓK:
	a, b: SZÖVEG,
	n: EGÉSZ

BE: a, b
KI: a[0:(a @ b)]
KI: " "
KI: a[(a @ b)+|b|:|a|]

PROGRAM_VÉGE
```
# 2. Vegyes feladatok
## 2.9.plang
> Sorold fel azokat a másodfokú egyenleteket, amelyek minden együtthatója 0 és 10 közötti egész szám, és pontosan egy megoldása van.
```PlanG
PROGRAM p
VÁLTOZÓK:
	a, b, c: EGÉSZ

a := 0
CIKLUS AMÍG a <= 10
	a := a + 1
	b := 0
	CIKLUS AMÍG b <= 10
		b := b + 1
		c := 0
		CIKLUS AMÍG c <= 10
			c := c + 1
			HA ((b^2) - (4*a*c)) = 0 AKKOR
				KI: a, "x^2+", b, "x+", c, SV
			HA_VÉGE
		CIKLUS_VÉGE
	CIKLUS_VÉGE
CIKLUS_VÉGE
PROGRAM_VÉGE
```
## 2.10.plang
> Add meg a Pascal-háromszög első N sorát.
```PlanG
PROGRAM a
VÁLTOZÓK:
	n, k, j, a, b, c, r: VALÓS

BE: r
n := 0
KI: "1", SV
CIKLUS AMÍG n < r - 1
	k := 0
	n := n + 1
	CIKLUS AMÍG k < n
		a := 1
		b := 1
		c := 1
		j := 1
		
		CIKLUS AMÍG j <= n
			a := a * j
			j := j + 1
		CIKLUS_VÉGE
		j := 1
		
		CIKLUS AMÍG j <= k
			b := b * j
			j := j + 1
		CIKLUS_VÉGE
		j := 1

		CIKLUS AMÍG j <= n - k
			c := c * j
			j := j + 1
		CIKLUS_VÉGE
		j := 1

		KI: EGÉSZ (a / (b * c)), " "
		k := k + 1
	CIKLUS_VÉGE
	KI: "1"
	KI: SV
CIKLUS_VÉGE
PROGRAM_VÉGE
```
## 2.13a.plang
> Egy két tagú névnek add meg a monogrammját.
```PlanG
PROGRAM a
VÁLTOZÓK:
	a: SZÖVEG

BE: a
KI: NAGY a[0], ". ", NAGY a[a @ ' ' + 1], "."

PROGRAM_VÉGE
```
## 2.13b.plang
> Egy akárhány tagú névnek add meg a monogrammját.
```PlanG
PROGRAM a
VÁLTOZÓK:
	a: SZÖVEG,
	i: EGÉSZ

BE: a
KI: NAGY a[0], "."

i : = 0
CIKLUS AM�G i < |a|
	HA a[i] = ' ' AKKOR
		KI: " ", NAGY a[i+1], "."
	HA_VÉGE
	i := i + 1
CIKLUS_VÉGE
PROGRAM_VÉGE
```
## 2.14a.plang
> Egy tetszőleges szövegben keresd meg az "alma" szó első előfordulását, és cseréld le a "körte" szóra.
```PlanG
PROGRAM p
VÁLTOZÓK:
	a: SZÖVEG

BE: a
KI: a[0 : a @ "alma"], "körte", a [(a @ "alma") + 4: |a|]

PROGRAM_VÉGE
```
## 2.14b.plang
> Az "alma" és "körte" szavak helyett tetszőleges szót lehessen megadni.
```PlanG
PROGRAM p
VÁLTOZÓK:
	a, b, c: SZÖVEG

BE: a, b, c
KI: a[0 : a @ b], c, a [(a @ b) + |b|: |a|]

PROGRAM_VÉGE
```
## 2.14c.plang
> Az összes előfordulást cseréld le.
```PlanG
PROGRAM p
VÁLTOZÓK:
	a, b, c: SZÖVEG,
	i: EGÉSZ

BE: a, b, c

i := 0
CIKLUS AMÍG i < |a|
	HA a @ b = i AKKOR
		KI: c
		a[i] := ' '
		i := i + |b|
	KÜLÖNBEN
		KI: a[i]
		i := i + 1
	HA_VÉGE
CIKLUS_VÉGE
PROGRAM_VÉGE
```
## 2.15.plang
> Egy tetszőleges szöveg minden szavát alakítsd át nagybetűvel kezdődőre.
```PlanG
PROGRAM p
VÁLTOZÓK:
	a: SZÖVEG,
	i: EGÉSZ

BE: a
KI: NAGY a[0]

i := 1
CIKLUS AMÍG i < |a|
	HA a[i - 1] = ' ' AKKOR
		KI: NAGY a[i]
	KÜLÖNBEN
		KI: a[i]
	HA_VÉGE
	i := i + 1
CIKLUS_VÉGE
PROGRAM_VÉGE
```
## 2.16a.plang
> Egy tetszőleges szövegből töröld ki az "alma" szó összes előfordulását.
```PlanG
PROGRAM p
VÁLTOZÓK:
	a: SZÖVEG,
	n: EGÉSZ

be: a
n := 0
CIKLUS AMÍG n < |a|
	HA a[n:|a|] @ "alma" = 0 AKKOR
		n := n + 4
	KÜLÖNBEN
		KI: a[n]
		n := n + 1
	HA_VÉGE
CIKLUS_VÉGE
PROGRAM_VÉGE
```
## 2.16b.plang
> Az "alma" helyett tetszőleges szót lehessen megadni.
```PlanG
PROGRAM p
VÁLTOZÓK:
	a, b: SZÖVEG,
	n: EGÉSZ

be: a, b

n := 0
CIKLUS AMÍG n < |a|
	HA a[n:|a|] @ b = 0 AKKOR
		n := n + |b|
	KÜLÖNBEN
		KI: a[n]
		n := n + 1
	HA_VÉGE
CIKLUS_VÉGE
PROGRAM_VÉGE
```
## 2.17a.plang
> Döntsd el egy szövegről, hogy ugyanazzal a karekterrel kezdődik-e, mint amivel végződik.
```PlanG
PROGRAM p
VÁLTOZÓK:
	a: SZÖVEG,
	x, y: EGÉSZ

be: a
x := a @ "(" + 1
y := a @ ")"
KI: a[x:y]

PROGRAM_VÉGE
```
## 2.17b.plang
> Azt is fogadd el egyezésnek, ha az egyik kisbetű, a másik nagybetű (pl. nagy A-val kezdődik, kis a-ra végződik).
```PlanG
PROGRAM p
VÁLTOZÓK:
	a: SZÖVEG,
	x, y: EGÉSZ

be: a

x := a @ "(" + 1
y := a @ ")"

HA x = |a| VAGY y = |a| AKKOR
	KI: "HIBA"
KÜLÖNBEN
	KI: a[x:y]
HA_VÉGE
PROGRAM_VÉGE
```
## 2.18.plang
> Egy tetszőleges szövegben alakítsd át a kisbetűket nagybetűkké, a nagybetűket pedig kisbetűkké.
```PlanG
PROGRAM a
VÁLTOZÓK:
	a: SZÖVEG,
	i: EGÉSZ

BE: a

i : = 0
CIKLUS AMÍG i < |a|
	HA a[i] = NAGY a[i] AKKOR
		a[i] := KIS a[i]
	KÜLÖNBEN
		a[i] := NAGY a[i]
	HA_VÉGE
	i := i + 1
CIKLUS_VÉGE

KI: a

PROGRAM_VÉGE
```
## 2.20.plang
> Fordíts meg egy tetszőleges egész számsort.
```PlanG
PROGRAM p
VÁLTOZÓK:
	a: SZÖVEG,
	n: EGÉSZ

be: a

n := 0
CIKLUS AMÍG n < |a|
	KI: a[|a| - n - 1]
	n := n + 1
CIKLUS_VÉGE
PROGRAM_VÉGE
```
## 2.26a.plang
> Add meg egy természetes szám prímtényezős felbontását.
```PlanG
PROGRAM a
VÁLTOZÓK:
	a, i: EGÉSZ

BE: a
CIKLUS AMÍG NEM (a = 1)
	i := 2
	CIKLUS AMÍG i < a + 1
		HA a MOD i = 0 AKKOR
			KI: i, SV
			a := a DIV i
			i := 1
		HA_VÉGE
		i := i + 1
	CIKLUS_VÉGE
CIKLUS_VÉGE
PROGRAM_VÉGE
```
## 2.26b.plang
> Az első N természetes szám felbontását add meg.
```PlanG
PROGRAM a
VÁLTOZÓK:
	n, m, a, i: EGÉSZ

BE: n

a := 1
CIKLUS AMÍG a <= n
	m := a
	HA a = 1 AKKOR
		KI: a, ": ", a, SV
	KÜLÖNBEN
		KI: a, ": "
	HA_VÉGE
	
	CIKLUS AMÍG NEM (a = 1)
		i := 2
		CIKLUS AMÍG i < a + 1
			HA a MOD i = 0 AKKOR
				KI: i, " "
				a := a DIV i
				i := 1
			HA_VÉGE
			i := i + 1
		CIKLUS_VÉGE
		KI: SV
	CIKLUS_VÉGE
	a := m + 1
CIKLUS_VÉGE
PROGRAM_VÉGE
```
## 2.32.plang
> Fésülj össze két monoton sorozatot fájlból.
```PlanG
PROGRAM a
VÁLTOZÓK:
	fa, fb: BEFÁJL,
	a, b: EGÉSZ,
	novekvo: LOGIKAI

MEGNYIT fa: "a"
MEGNYIT fb: "b"

BE fa: a
BE fb: b

CIKLUS AMÍG NEM VÉGE fa ÉS NEM VÉGE fb
	HA a <= b AKKOR
		KI: a
		BE fa: a
	KÜLÖNBEN
		KI: b
		BE fb: b
	HA_VÉGE
CIKLUS_VÉGE

CIKLUS AMÍG NEM VÉGE fa
	KI: a
	BE: fa: a
CIKLUS_VÉGE

CIKLUS AMÍG NEM VÉGE fb
	KI: b
	BE: fb: b
CIKLUS_VÉGE
PROGRAM_VÉGE
```
# 3. Programozási tételek
## 3.2.plang
> Add meg egy természetes szám osztóinak összegét.
```PlanG
PROGRAM számláló
VÁLTOZÓK:
	n, i, összeg: EGÉSZ

összeg := 0
BE: n

i := 2
CIKLUS AMÍG i < n
	HA n MOD i = 0 AKKOR
		összeg := összeg + 1
	HA_VÉGE
	i := i + 1
CIKLUS_VÉGE
KI: összeg

PROGRAM_VÉGE
```
## 3.4.plang
> Add meg egy természetes szám legnagyobb valódi osztóját.
```PlanG
PROGRAM maximum
VÁLTOZÓK:
	n, i, max: EGÉSZ

max := 0
BE: n

i := 2
CIKLUS AMÍG i < n
	HA n MOD i = 0 ÉS i > max AKKOR
		max := i
	HA_VÉGE
	i := i + 1
CIKLUS_VÉGE

HA max = 0 AKKOR
	KI: "nincs valódi osztója"
KÜLÖNBEN
	KI: max
HA_VÉGE

PROGRAM_VÉGE
```
## 3.8b.plang
> Adj össze tetszőleges számú számot.
```PlanG
PROGRAM p
VÁLTOZÓK:
	m, i, a, összeg: EGÉSZ  

BE: m
összeg := 0

i := 0
CIKLUS AMÍG i < m
	BE: a
	összeg := összeg + a
	i := i + 1
CIKLUS_VÉGE
KI: összeg

PROGRAM_VÉGE
```
## 3.10.plang
> Add meg egy tetszőleges egész számsorról, hogy hány eleme kisebb az átlagánál.
```PlanG
PROGRAM p
VÁLTOZÓK:
	szamok: VALÓS[32],
	n, a, atlag, osszeg: VALÓS,
	i, szamlalo: EGÉSZ

BE: n
i := 0
CIKLUS AMÍG i < n
	BE: a
	szamok[i] := a
	i := i + 1
CIKLUS_VÉGE

i := 0
osszeg := 0
CIKLUS AMÍG i < n
	osszeg := osszeg + szamok[i]
	i := i + 1
CIKLUS_VÉGE

atlag:= osszeg / n

i := 0
szamlalo := 0
CIKLUS AMÍG i < n
	HA szamok[i] < atlag AKKOR
		szamlalo := szamlalo + 1
	HA_VÉGE
	i := i + 1
CIKLUS_VÉGE

KI: szamlalo

PROGRAM_VÉGE
```
## 3.13.plang
> Add meg egy tetszőleges pozitív számsorozat elemeinek a négyzetgyök-összegét.
```Plang
PROGRAM p
VÁLTOZÓK:
	n, a, i: EGÉSZ,
	osszeg: VALÓS

BE: n
i := 0
osszeg := 0
CIKLUS AMYG i < n
	BE: a
	osszeg := osszeg + (a^2)
	i := i + 1
CIKLUS_VÉGE

KI: osszeg

PROGRAM_VÉGE
```
## 3.15.plang
> Egy szigorúan növő egész számsorban add meg a legnagyobb ugrást (szomszédos elemek közötti legnagyobb előforduló különbséget). Nem monoton számsorra is adj helyes eredményt.
```PlanG
PROGRAM p
VÁLTOZÓK:
	bf: BEFÁJL,
	a, b, min: EGÉSZ

min := 0
MEGNYIT bf: "a"
BE bf: a, b

CIKLUS AMÍG NEM VÉGE bf
	HA min = 0 AKKOR
		min := b - a
	KÜLÖNBEN
		HA b - a < min AKKOR
			min := b - a
		HA_VÉGE
	HA_VÉGE
	a := b
	BE bf: b
CIKLUS_VÉGE

LEZÁR bf
KI: min

PROGRAM_VÉGE
```
## 3.16.plang
> Add meg egy tetszőleges egész számsorban a szomszédos elemek átlagos különbségét.
```PlanG
PROGRAM számláló
VÁLTOZÓK:
	n, i, a, előző: EGÉSZ,
	összeg: VALÓS

összeg := 0

BE: n
BE: a
előző := a

i := 0
CIKLUS AMÍG i < n - 1
	BE: a
	összeg := előző - a
	i := i + 1
CIKLUS_VÉGE
KI: összeg / (n - 1)

PROGRAM_VÉGE
```
## 3.18.plang
> Add meg egy tetszőleges egész számsorban a prímszámok számát.
```PlanG
PROGRAM p
VÁLTOZÓK:
	m, i, j, a, hány: EGÉSZ,
	van: LOGIKAI

BE: m
hány := m

i := 0
CIKLUS AMÍG i < m
	BE: a
	
	j := 2
	van := HAMIS
	CIKLUS AMÍG j < a ÉS NEM van
		HA a MOD j = 0 AKKOR
			van := IGAZ
			hány := hány - 1
		HA_VÉGE
		j := j + 1
	CIKLUS_VÉGE
	i := i + 1
CIKLUS_VÉGE
KI: hány

PROGRAM_VÉGE
```
## 3.21.plang
> 1. Egy tetszőleges szövegről add meg, hány kis "a" betű van benne.
```PlanG
PROGRAM p
VÁLTOZÓK:
	n: SZÖVEG,
	i, számláló: EGÉSZ

BE: n
számláló := 0

i := 0
CIKLUS AMÍG i < |n|
	HA n[i] = 'a' AKKOR
		számláló := számláló + 1
	HA_VÉGE
	i := i + 1
CIKLUS_VÉGE
KI: számláló

PROGRAM_VÉGE
```
## 3.24.plang
> Add meg egy tetszőleges szövegből a leghosszabb sort.
```PlanG
PROGRAM p
VÁLTOZÓK:
	a, max: SZÖVEG,
	n, i, számláló: EGÉSZ

BE: n
BE: a
max := a

i := 0
CIKLUS AMÍG i < n - 1
	BE: a
	HA |a| > |max| AKKOR
		max := a
	HA_VÉGE
	i := i + 1
CIKLUS_VÉGE

KI: max
PROGRAM_VÉGE
```
## 3.25.plang
> Döntsd el egy tetszőleges szövegről, hogy a sorai ABC-sorrendben vannak-e.
```PlanG
PROGRAM p
VÁLTOZÓK:
	m, i: EGÉSZ,
	a: SZÖVEG,
	előtte: KARAKTER,
	feltétel: LOGIKAI

BE: m, a, a
előtte := a[0]
feltétel := IGAZ

i := 0
CIKLUS AMÍG i < m - 1 ÉS feltátel
	BE: a
	HA előtte > a[0] AKKOR
		feltétel := HAMIS
	HA_VÉGE
	i := i + 1
	
	előtte := a[0]
CIKLUS_VÉGE
KI: feltetel

PROGRAM_VÉGE
```
## 3.34.plang
> Tetszőleges, a csúcsai koordinátáival adott sokszögnek add meg a kerületét.
```PlanG
PROGRAM p
VÁLTOZÓK:
	n, i, x, y, előző_x, előző_y, első_x, első_y: EGÉSZ,
	összeg: VALÓS

BE: n
összeg := 0

BE: első_x, első_y
előző_x := első_x
előző_y := első_y

i := 0
CIKLUS AMÍG i < n -1
	BE: x, y
	összeg := összeg + (((x - előző_x)^2) + ((y - előző_y)^2))^0.5
	előző_x := x
	előző_y := y
	i := i + 1
CIKLUS_VÉGE

összeg := összeg + (((x - első_x)^2) + ((y - első_y)^2))^0.5
KI: összeg

PROGRAM_VÉGE
```
## 3.36.plang
> Tetszőleges, koordinátákkal adott pontsorozatban add meg az origótól legtávolabb eső pontot.
```PlanG
PROGRAM p
VÁLTOZÓK:
	n, i, x, y, max_x, max_y: EGÉSZ,
	max, uj: VALÓS

BE: n, x, y
max_x := x
max_y := y

i := 0
CIKLUS AMÍG i < n -1
	BE: x, y
	max := (((max_x)^2) + ((max_y)^2))^0.5
	uj := (((x)^2) + ((y)^2))^0.5
	
	HA uj > max AKKOR
		max_x := x
		max_y := y
	HA_VÉGE
	i := i + 1
CIKLUS_VÉGE
KI: "(",max_x, "; ", max_y, ")"

PROGRAM_VÉGE
```
# 4. Rekordok
# 5. Tömbös feladatok
## 5.1.plang
> Véletlen tömb: egy tömb elemeit töltsd fel véletlen számokkal. _(A következő feladatok akár véletlennel, akár másképp feltöltött vektorokkal foglalkoznak)_
```Plang
PROGRAM p
VÁLTOZÓK:
	tomb: EGÉSZ[10],
	i: EGÉSZ

i := 0
CIKLUS AMÍG i < |tomb|
	tomb[i] := RND 10
	i := i + 1
CIKLUS_VÉGE
PROGRAM_VÉGE
```
## 5.2.plang
> Vektor átlaga
```Plang
PROGRAM p
VÁLTOZÓK:
	tomb: VALÓS[3],
	osszeg: VALÓS,
	i: EGÉSZ

i := 0
osszeg := 0
CIKLUS AMÍG i < |tomb|
	tomb[i] := RND 10
	osszeg := osszeg + tomb[i]
	i := i + 1
CIKLUS_VÉGE

KI: osszeg / i

PROGRAM_VÉGE
```
## 5.3.plang
> Vektor szórása (átlagtól való eltérések átlaga)
```PlanG
PROGRAM p
VÁLTOZÓK:
	tomb: VALÓS[3],
	osszeg, a: VALÓS,
	i: EGÉSZ

i := 0
osszeg := 0
CIKLUS AMÍG i < |tomb|
	tomb[i] := RND 10
	osszeg := osszeg + tomb[i]
	i := i + 1
CIKLUS_VÉGE

a := osszeg / i

i := 0
osszeg := 0
CIKLUS AMÍG i < |tomb|
	osszeg := osszeg + (tomb[i] - a)^2
	i := i + 1
CIKLUS_VÉGE

KI: (osszeg / i)^0.5

PROGRAM_VÉGE
```
## 5.4.plang
> Van-e két egyforma elem a vektorban?
```PlanG
PROGRAM p
VÁLTOZÓK:
	tomb: EGÉSZ[3],
	i, j: EGÉSZ

i := 0
CIKLUS AMÍG i < |tomb|
	tomb[i] := RND 10
	i := i + 1
CIKLUS_VÉGE

i := 0
CIKLUS AMÍG i < |tomb|
	j := 0
	CIKLUS AMÍG j < |tomb|
		HA NEM (i = j) ÉS tomb[i] = tomb[j] AKKOR
			KI: "van, a ", i +1, ". és a ", j+1, ". elem"
			j := |tomb|
			i := |tomb|
		HA_VÉGE
		j := j + 1
	CIKLUS_VÉGE
	i := i + 1
CIKLUS_VÉGE
PROGRAM_VÉGE
```
## 5.5.plang
> Vektor permutálása véletlenszerűen.
```PlanG
PROGRAM p
VÁLTOZÓK:
	tomb: EGÉSZ[3],
	i, j, a: EGÉSZ

i := 0
CIKLUS AMÍG i < |tomb|
	tomb[i] := RND 10
	i := i + 1
CIKLUS_VÉGE

i := 0
CIKLUS AMÍG i < |tomb|
	j := RND |tomb|
	a := tomb[i]
	tomb[i] := tomb[j]
	tomb[j] := tomb[i]
	i := i + 1
CIKLUS_VÉGE
PROGRAM_VÉGE
```