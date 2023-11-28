---
aliases:
  - Ítéletkalkulus
  - Kijelentéskalkulus
---
## Szintaxis [^1]
A leírott kifejezés helyességét határozza meg.
### Jelkészlet
- betűk (ítéletváltozók) - atomok
- I(gaz), H(amis) (konstansok) - atomok
- $\neg, \lor, \land, \implies$ - műveleti szimbólumok
- zárójelek
### Formulaképzés
- minden atom formula
	Például: $\alpha, \beta$ formula, akkor $\neg\alpha$, $\alpha\implies\beta$... is formulák
- az itéletváltozók és műveleti szimbólumok alkalmazásával összetett formulákat tudunk képezni
(magyar betűkkel jelöljük az atomi formukákat, görög betűkkel az összetett formulákkal)
## Szemantika [^1]
A helyes kifejezés jelentését határozza meg.
## Interpretáció [^2]
Egy függvény változóihoz hozzárendeljük a lehetséges igazságértékek valamelyikét.
- $n$ változó esetén a lehetőségek száma: $n^2$
## Modell
Olyan [[Nulladrendű logika#Interpretáció [ 2]|interpretáció]], amiben a [[Nulladrendű logika#Formulaképzés|formula]] igaz.
## Tautológia
Minden [[Nulladrendű logika#Interpretáció|interpretációban]] igaz.
## Kontradikció
Ellentmondás, a [[Nulladrendű logika#Tautológia|tautológia]] ellenpárja. Minden [[#Interpretáció|interpretációban]] hamis.
## Logikai műveletek
### Konjunkció - metszet - és
Jele: $\land$

| $A$ | $B$ | $A\land B$ |
|---|---|---|
|0|0|0|
|1|0|0|
|0|1|0|
|1|1|1|
### Diszjunkció - unió - vagy
Jele: $\lor$

| $A$ | $B$ | $A\lor B$ |
|---|---|---|
|0|0|0|
|1|0|1|
|0|1|1|
|1|1|1|
### Komplementer
Jele: $\neg$

| $A$ | $\neg A$ |
|---|---|
|0|1|
|1|0|
### Implikáció
Jele: $\implies$

| $A$ | $B$ | $A\implies B$ |
|---|---|---|
|0|0|1|
|0|1|1|
|1|0|0|
|1|1|1|
### Ekvivalencia
Jele: $\equiv$

| $A$ | $B$ | $A\equiv B$ |
|---|---|---|
|0|0|1|
|1|0|0|
|0|1|0|
|1|1|1|
#### Formulák ekvivalenciája
Két formula ekvivalens amennyibe az igazságértékük minden interpretációban megegyezik.
## Formalizálás
A formalizálás során a kijelentéseket matematikai nyelvre fogalmazzuk meg.
## Normálformák
Az adott műveleteket úgy alakítjuk át, hogy azokat adott sorrendben végezzük el.
### Diszjunktív normálforma
### Konjunktív normálforma
Utoljára éselünk. Ehhez a következő átalakításokra lesz szükségünk:
- $A \oplus B$: $(A \lor B)\land(\neg A \lor\neg B)$
- $A\equiv B$: $(A \implies B)\land(B \implies A)$
- $A\implies B$: $\neg A\lor B$
- $A\lor(B\land C)$: $(A\lor B)\land(A\lor C)$
## Klóz
[[Nulladrendű logika#Konjunktív normálforma|Konjunktív]] és [[Nulladrendű logika#Diszjunktív normálforma|diszjunktív normálformák]] esetén is amiket össze[[Nulladrendű logika#Konjunkció - metszet - és|és]]elünk ([[Nulladrendű logika#Konjunktív normálforma|konjunktív normálformák]] esetén), vagy össze[[Nulladrendű logika#Diszjunkció - unió - vagy|vagy]]olunk ([[Nulladrendű logika#Diszjunktív normálforma|diszjunktív normálforma]] esetén) klózoknak hívunk.
# Rezolúció
Rezolúciót akkor használunk, amikor azt szeretnénk belátni, hogy egy kifejezés minden interpretációban igaz, vagyis tautológia.
Ilyenkor a kifejezés megfordítására próbálunk igaz példát hozni, indirekt bizonyítást alkalmazunk. Mivel a tautológia megfordítása a kontradikció, amennyiben az eredeti állításunk igaz, nem fogunk tudni modellt találni a megfordítására.
## Gyakorlati lépések
1. [[Nulladrendű logika#Formalizálás|Formalizáció]]
2. Premisszák (feltételek) felírása egymás alá
3. Következmény [[Nulladrendű logika#Komplementer|tagadása]]
4. Tagadott következmény [[Nulladrendű logika#Konjunktív normálforma|konjunktív normálformára hozása]]
5. [[Nulladrendű logika#Klóz|Klózok]] egymás alá írása
6. Kiejtegetés
7. Üres klóz
# Következmény
Jele: $\models$
- Kontradikció következménye bármi
- Tautológia következménye tautológia
$$\alpha\models\beta\Leftrightarrow\alpha\implies\beta\equiv1\Leftrightarrow\alpha\land\neg\beta\equiv0$$
# Következtetési sémák bizonyítása
## Modus Ponens
| $A$ | $B$ | $A\implies B$ |
|---|---|---|
|0|0|1|
|1|0|0|
|0|1|0|
|**1**|**1**|**1**|
A negyedik sorban igazak a feltételek, itt igaz a következmény is.
## Modus Tollens
| $A$ | $B$ | $A\implies B$ | $\neg A$ | $\neg B$ |
|---|---|---|---|---|
|0|0|1|1|1|
|1|0|0|0|1|
|0|1|0|1|0|
|1|1|1|0|0|
Az első sorban igazak a feltételek, itt igaz a következmény is.
## Diszjunktív szillogizmus
| $A$ | $B$ | $A\lor B$ | $\neg A$ |
|---|---|---|---|
|0|0|0|1|
|0|1|1|1|
|1|0|1|0|
|1|1|1|0|
A második sorban igazak a feltételek, itt igaz a következmény is.
## Hipotetikus szillogizmus
| $A$ | $B$ | $C$ | $A\implies B$ | $B\implies C$ | $A\implies C$ |
|---|---|---|---|--|--|
|0|0|0|1|1|1|
|0|0|1|1|1|1|
|0|1|0|1|0|0|
|0|1|1|1|1|1|
|1|0|0|0|1|1|
|1|0|1|0|1|1|
|1|1|0|1|0|0|
|1|1|1|1|1|1|
Minden sorban amiben a feltételek igazak igaz a következmény is.
# Feladatok
- [[LA Feladatgyujtemeny.pdf#page=11|Lineáris Algebra Feladatgyűjtemény 11. oldal.]]
- [[06 Nulladrendű logika.pdf|06 Gyakorlat feladatsor]]
- [[07-08 Rezolúció.pdf|07-08 Gyakorlat feladatsor]]
- [[09 Következmény és Rezolúció.pdf|09 Gyakorlat feladatsor]]
### Megoldások
- [[06 Megoldás.pdf|06 Gyakorlat feladatsor megoldás]]
- [[07-08 Megoldás.pdf|07-08 Gyakorlat feladatsor megoldás]]
- [[09 Megoldás.pdf|09 Gyakorlat feladatsor megoldás]]
# Hasznos dokumentumok
- [[Matematikai Logika.pdf]]

[^1]: [[DM Tankonyv.pdf#page=32|Diszkrét Matematika tankönyv: 32. oldal]]
[^2]: [[DM Tankonyv.pdf#page=33|Diszkrét Matematika tankönyv: 33. oldal]]