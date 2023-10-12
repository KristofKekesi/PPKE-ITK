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

Jelölésük:
- ∀: minden
- ∃: létezik
- ∃!: egyértelműen létezik

## Műveleti alaptulajdonságok
### Asszociativitás
Jelentése: csoportosíthatóság. Például: `(x + y) + z = x + (y + z)`.
- összeadás
- szorzás
### Kommutativitás
Jelentése: felcserélhetőség. Például: `x + y = y + x`.
- összeadás
- szorzás
### Disztributivitás
#TODO 


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

# Korlátosság
Legyen `H⊂R` - H halmaz a valós számoknak részhalmaza
### Alulról korlátos,
ha `∃K ∈ R`(ez lesz az alsó korlát), amire `x ≤ K ∀x ∈ H`.
### Felülről korlátos
#TODO 
## Korlátos,
ha a halmaz alulról és felülről is korlátos.
### Supremum
#TODO 
## Infimum
#TODO 