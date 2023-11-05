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
### Konjunktív normálforma
### Diszjunktív normálforma
## Doepikon következmény
A B formula az d formuka logikai következménye, ha B igaz minden olyan interpretációra, ahol d igaz.
Jele: #TODO
## Modus Ponens
#TODO 

Nulladrendű logika = ítéletkalkulus = kijelentéskalkulus
Logika helyes következtetése, sémák elmélete
Pl: Ha esik az eső sáros az út <- 1. premissza
Esik az eső. <- 2. premissza
- - - - - - - - - - -
Sáros az út. <- következtetés

# Feladatok
- [[06 Gyakorlat.pdf|06 Gyakorlat feladatsor]]
- [[07-08 Gyakorlat.pdf|07-08 Gyakorlat feladatsor]]
- [[09 Gyakorlat.pdf|09 Gyakorlat feladatsor]]
# Hasznos dokumentumok
- [[Matematikai Logika.pdf]]

[^1]: [[DM Tankonyv.pdf#page=32|Diszkrét Matematika tankönyv: 32. oldal]]
[^2]: [[DM Tankonyv.pdf#page=33|Diszkrét Matematika tankönyv: 33. oldal]]