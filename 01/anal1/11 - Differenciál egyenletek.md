---
Óra neve: Matematikai analízis 1.
Előadó: Dr. Vágó Zsuzsanna Márta
Dátum: 2023 Nov. 27.
aliases:
  - DE
---
## Egyenlet
**Jelölés**:
$$f(x)=e^x\quad\Rightarrow\quad f'(x)=e^x$$
$$y=f(x)\quad\quad y'=e^x$$
$$y=y(x)\quad\quad y'=y$$
**Példa**:
$$g(x)=e^{ax}\quad(a≠0)\quad\quad g'(x)=a\cdot e^{ax}$$
$$y'=ay\quad\quad y=y(x)=?$$
**Állítás**:
Tegyük fel, hogy van olyan $y=y(x)$, amire
$$y'=ay\quad\quad$$
## Differenciálegyenlet (DE) [^3]
Olyan egyenlet (=összefüggés), amely
- megoldása egy függvény,
- szerepel benne az ismeretlen deriváltja
**Legegyszerűbb differenciálegyenlet**:
$$y'=f(x)\quad\Rightarrow\quad y=\int{f(x)}dx$$
Itt $f$ adott függvény.
### Általános megoldás [^4]
- mindig van benne paraméter, ezért végtelen sok függvényt jelent
**Például**:
$$y'=2x\quad\Rightarrow\quad y=x^2+c\quad(c\in R)$$
### Partikuláris megoldás [^4]
Amikor egy konkrét megoldást keresünk.
### Differenciálegyenlet jellemzői [^1]
- Két betű ($x$: független változó; $y$: függő változó)
- **Rendje**: a DE-ben az ismeretlen függvény legmagasabb deriváltjának a száma
	- Elsőrendű DE: $y'=ay$
	- Másodrendű DE: $y''+y=0\quad\big(\Rightarrow\quad y_1=\sin(x)\quad y_2=cos(x)\big)$
	- …
## Elsőrendű differenciálegyenlet általános alakja [^1]
$$y'=f(x,y)$$
Ahol $f(x,y)$ adott kétváltozós függvény.
## Cauchy feladat / Kezdetiérték feladat [^1]
A megoldás egy intervallumon értelmezett differenciálható függvény: $y:I\to R$,
- differenciálható az $I\subset R$ intervallumon
$$y'(x)=f\big(x,y(x)\big)\quad\forall x\in I$$
## Szeparábilis / szétválasztható differenciálegyenlet [^2]
Szeparábilis differenciálegyenlet amennyiben az egyenlet jobb oldalán lévő $f(x,y)$ függvényben az $x$ és az $y$ a következőképpen szétválasztható:
$$y'=f(x,y)=\frac{\alpha(x)}{\beta(y)}\quad\quad\beta(y)≠0.$$
Itt $\alpha$ és $\beta$ adott függvények.
## Lineáris differenciálegyenlet (LDE)
Ha a differenciálegyenlet jobboldalán szereplő $f(x,y)$ lineáris $y$-ra.
$$y'=f(x,y)=a(x)y+b(x)$$
Itt $a(x)$ és $b(x)$ adott függvények.
### Homogén lineáris differenciálegyenlet
Ha $b(x)=0$.
**Tétel**:
$y'=a(x)y$ egyenlet megoldása vektortér. Ez a vektortér 1D-s.
### Inhomogén lineáris differenciálegyenlet
Ha $b(x)≠0$.

[^1]: [[Analízis 1. (2023).pdf#page=172|Analízis 1. Jegyzet 166. oldal]]
[^2]: [[Analízis 1. (2023).pdf#page=175|Analízis 1. Jegyzet 169. oldal]]
[^3]: [[Analízis 1. (2023).pdf#page=170|Analízis 1. Jegyzet 164. oldal]]
[^4]: [[Analízis 1. (2023).pdf#page=171|Analízis 1. Jegyzet 165. oldal]]