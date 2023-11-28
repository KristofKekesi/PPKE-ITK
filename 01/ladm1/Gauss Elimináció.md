---
aliases:
  - Gauss-Jordan Elimináció
---
# Vektorok (előismeret)
- Független vektorok: 
	- 2 vektor esetén: amennyiben nem párhuzamosak,
	- 3 vektor esetén: amennyiben nem egysíkúak,
	- 4 vektor esetén: amennyiben nem egyhipersíkúak.
- Összefüggő vektorok: amennyiben nem függetlenek.
	- Ha több sor van mint oszlop.
# Gauss-Jordan Elimináció [^1]
Egyenletrendszer megoldása mátrix alakú felírása alapján.
- ==Sorokat nem cserélhetünk fel==, oszlopokat igen
[Mátrix számológép (Gauss elimináció megoldásához)](https://matrixcalc.org/slu.html)
## Vezérelem [^2]
Minden sorban és oszlopban kiválaszthatunk egy (nem nulla) számot.
## Rang [^2]
[[#Vezérelem [ 2]|Vezérelem]]ek száma a megoldásvektoron kívűl, az együttható ($A$) oldaláról.
- Ez adja meg a képtér dimenzióját
- jele: $\text{rang}(A)$
## Bővített mátrix rangja
A [[#Vezérelem [ 2]|vezérelem]]ekek száma mindkét, az együttható oldaláról és a megoldásvektor oldaláról is.
- Jele: $\text{rang}(A|b)$
## Szabadsági fok [^4]
Más néven a magtér dimenziója. A szabad változók ([[#vezérelem [ 2]|vezérelem]]mel nem rendelkező oszlopok) száma.
## Nullsor [^3]
Olyan sor a mátrixban, ahol minden szám nulla. (még a megoldáshalmazban is).
- Ha azonos az oszlopok száma és a sorok száma azonos, ===jelentése: voltak benne összefüggő vektorok==
## Tilos sor [^4]
Olyan sor ahol az együttható oldalán ($A$) csak nullák vannak, míg a megoldáshalmaz ($b$) nem nulla.
- ==Jelentése: nem lesz megoldása az egyenletrendszernek.==
## Homogén egyenletrendszer
Ha a megoldásvektor ($b$) nulla, homogén egyenletrendszerről beszélünk.
- ==Jelentése: mindig lesz legalább egy megoldása. Ez a triviális megoldás, a nulla.==
## Inhomogén egyenletrendszer
Inhomogén egyenletrendszerről beszélünk ha nem [[#Homogén egyenletrendszer|homogén]], vagyis ha a megoldásvektor ($b$) nem nulla.
# Feladatok
- [[LA Feladatgyujtemeny.pdf#page=7|Lineáris Algebra Feladatgyűjtemény 7. oldal.]]
- [[01-02 Gauss elimináció.pdf|01-02 Gyakorlat feladatsor]]
- [[03 Gauss ellimináció.pdf|03 Gyakorlat feladatsor]]
- [[04-05 Gauss-Jordan elimináció.pdf|04-05 Gyakorlat feladatsor]]
- [[Gauss Elimináció]]
### Megoldások
- [[01-02 Megoldás.pdf|01-02 Gyakorlat feladatsor megoldás]]
- [[03 Megoldás.pdf|03 Gyakorlat feladatsor megoldás]]
- [[04-05 Megoldás.pdf|04-05 Gyakorlat feladatsor megoldás]]

![[Gauss Elimináció.png]]
[[Tárgyak#Miski Marcell||Miski Marcell]] féle infografika.
![[Gauss Elimináció metsző egyenesek.pdf]]
[[Tárgyak#Miski Marcell||Miski Marcell]] féle infografika.
![[Magtér.pdf]]
[[Tárgyak#Miski Marcell||Miski Marcell]] féle infografika.

---

[^1] [[LA Tankonyv.pdf#page=11|Lineáris Algebra Tankönyv 11. oldal]]
[^2] [[LA Tankonyv.pdf#page=12|Lineáris Algebra Tankönyv 12]]
[^3] [[LA Tankonyv.pdf#page=15|Lineáris Algebra Tankönyv 15. oldal]]
[^4] [[LA Tankonyv.pdf#page=16|Lineáris Algebra Tankönyv 16. oldal]]
