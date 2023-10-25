---
Óra neve: Matematikai Analízis 1.
Előadó: Dr. Vágó Zsuzsanna Márta
Dátum: 2023 Okt. 09.
---
# Számhalmazok
## N: természetes számok halmaza
- jele: N (natural szóból ered)
- Legkisebb eleme az 1
- Minden elem után van következő

### Teljes indukció (bizonyítási elv)
Legyen A<sub>n</sub> valamilyen állítás minden n természetes számra. Ha:
1. A<sub>1</sub> teljesül, és
2. A<sub>k+1</sub> mindig igaz A<sub>k</sub> teljesülése esetén,
akkor a fenti A<sub>n</sub> tulajdonság teljesül minden n-re.

### Természetes számok halmazának bővítése
- összeadás: Nem vezet ki a természetes számok halmazából
- kivonás: Kivezet a természetes számok halmazából -> Egész számok halmaza

## Z: egész számok halmaza
- jele: Z (zahl szóból ered)
### Egész számok halmazának bővítése
- szorzás: Kivezet az egész számok halmazából -> Valós számok halmaza
- osztás: Kivezet az egész számok halmazából -> Valós számok halmaza

## R: Valós számok halmaza
- jele: R
- minden valós szám kifejezhető két egész szám osztásával

# Axiómák
- Alaptulajdonságok

## Kvantorok
Jelölésük:
- ∀: minden
- ∃: létezik
- ∃!: egyértelműen létezik
## Asszociativitás
Jelentése: csoportosíthatóság.
Például: `(x + y) + z = x + (y + z)`.
- összeadás
- szorzás
## Kommutativitás
Jelentése:  felcserélhetőség.
Például: `x + y = y + x`.
- összeadás
- szorzás
## Disztributivitás
Jelentése: műveletek összekapcsolódása.
Például: `(a + b) * c = (a * c) + (b * c)`.
## Műveleti alaptulajdonságok
1. Az összeadás [[01 - Valós számok bevezetése#Asszociativitás|asszociatív]]
2. `x + 0 = x; ∀x ∈ R`
3. `∀x ∈ R` van `∃u ∈ R` tartozik `x+u=0`. Ez az `x` szám ellentettje.
4. Az összeadás [[01 - Valós számok bevezetése#Kommutativitás|kommutatív]]
5. A szorzás [[01 - Valós számok bevezetése#Asszociativitás|asszociatív]]
6. `x * 1 = x`
7. `∀x ∈ R, x != 0` tartozik `∃u ∈ R`, melyre `u=1/x`. Ez a szám reciproka.
8. A szorzás [[01 - Valós számok bevezetése#Kommutativitás|kommutatív]]
9. A szorzás [[01 - Valós számok bevezetése#Disztributivitás|disztributív]] az összeadásra
## Rendezési reláció tulajdonságai
10. `∀x ∈ R` esetén  `x ≤ x` (a rendezési reláció reflexív)
11. `∀x != y` esetén az `x ≤ y` és `y ≤ x` közül pontosan egy igaz.
12. Ha `x ≤ y` és `y ≤ z` ⇒ `x ≤ y` (a rendezési reláció tranzitív)
13. Ha `x ≤ y` ⇒ `x + z ≤ y + z`
14. Ha `x ≤ y` és `0 ≤ z` ⇒ `x * z ≤ y * z`
15. Arcimedeszi axióma: Nincs nagyobb elem

## Cantor-féle axióma
16. Ha zárt intervallumok egy sorozata:
	I<sub>1</sub>=\[a<sub>1</sub>, b<sub>1</sub>\], I<sub>2</sub>=\[a<sub>2</sub>, b<sub>2</sub>\], ...
	melyek I<sub>1</sub> ⊇ I<sub>2</sub> ⊇ ...
	akkor az intervallumoknak __van közös pontja__.
	Más szóval, `∃c ∈ R` melyre `c ∈ Ik , ∀k ∈ N`
	
	Cantor axióma => irracionális számok is vannak

# Summa
$$\sum_{futóindex}^{meddig} tag$$
Például:
- Első `n` szám összege
$$\sum_{k=1}^{n} k$$
- Első `n` páros szám összege
$$\sum_{k=1}^{n} 2k$$
- Hárommal osztható kétjegyű számok összege
$$\sum_{k=4}^{33} 3k$$
- Száz és kétszáz közötti (nyílt intervallum) természetes számok reciprokainak az összege
$$\sum_{k=101}^{199}\frac{1}{k}$$
# Produktum
Röviden a summa működése összeadás helyett szorzással.
$$\prod_{futóindex}^{meddig} tag$$
# Korlátosság
Legyen `H⊂R` - H halmaz a valós számoknak részhalmaza
## Alulról korlátos,
ha `∃k ∈ R`(ez lesz az alsó korlát), amire `k ≤ x ∀x ∈ H`.
## Felülről korlátos
ha `∃K ∈ R`(ez lesz a felső korlát), amire `K ≥ x ∀x ∈ H`.
## Korlátos,
ha a halmaz alulról és felülről is korlátos.
## Supremum
A halmaz legkisebb felső korlátja.
Jele: `sup(H)`.
- Ha a H halmaznak az elemei közül van legnagyobb, akkor az a supremuma.
	`sup(H) = max(h)`
## Infimum
A halmaz legnagyobb alsó korlátja.
Jele: `inf(H)`.
- Ha a H halmaznak az elemei közül van legkisebb, akkor az az infimuma.
	`inf(H) = min(h)`
## Ekvivalens
Azonos.
#TODO 
# Környezet
Egy x<sub>0</sub> valós szám __Környezetei__ az $(x_0- ε; x_0 + ε)$ nyílt intervallumok, ahol $\epsilon > 0$ tetszőleges valós szám.
## Belső pont
Az $x_0 ∈ R$ pont a H halmaz belső pontja, ha $∃\epsilon > 0$. Amin $(x_0 − \epsilon, x_0 + \epsilon) ⊆ H$.
Jele: `int(H)` (az angol interior szóból).
## Külső pont
Az $x_0 ∈ R$ pont a H halmaz belső pontja, ha $∃\epsilon > 0$. Amin $(x_0 − \epsilon, x_0 + \epsilon) \cap H= \emptyset$.
Jele: `ext(H)` (az angol exterior szóból).
## Határpont
Az $x_0 ∈ R$ pont a H halmaz határpontja, ha $∃\epsilon > 0$. Ha a környezet tartalmaz H-n belüli (Belső pont) és H-n (Külső pont) kívüli pontokat is.
Jele: `∂(H)`

- A halmaz nyílt, ha minden pontja belső pont
- A halmaz zárt ha $∂H ⊆ H$
- A H halmaz lezárása $\overline{H} = H ∪ ∂H$