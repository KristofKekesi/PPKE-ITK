---
Óra neve: Matematikai analízis 1.
Előadó: Dr. Vágó Zsuzsanna Márta
Dátum: 2023 Nov. 09.
---
## Görbületek[^1]
### Konvex
$f: I\implies R$, konvex, ha minden $x_1<x_2\in[a, b]$ esetén
$$f((1-t)x_1+x_2)\leq(1-t)f(x_1)+tf(x_2)\quad\quad t\in[0,1].$$
Másszóval:
- A függvény bármely két pontját ha összekötjük, a szakaszuk a függvény fölött lesz.
### Konkáv
$f$ függvény konkáv, ha $-f$-ben [[07 - Függvények 5.#Konvex|konvex]].
Másszóval:
- A függvény bármely két pontját ha összekötjük, a szakaszuk a függvény alatt lesz.
### Inflexiós pont
$x_0\in D_f$ inflexiós pont, ha ebben a pontban vált a függvény [[07 - Függvények 5.#Konvex|konvex]]ből [[07 - Függvények 5.#Konkáv|konkáv]]ba vagy fordítva.
$$f''(x_0)=0$$
# Integrálszámítás
### Integrálszámítás I. alaptétele[^2]
Legyen $f,g: (a,b)\to R$ olyan differenciálható függvények, melyekre $f'(x)=g'(x)$ teljesül minden $x\in(a,b)$-re. Ekkor $\exists c\in R$, melyre
$$f(x)=g(x)+c\quad\quad\forall x\in(a,b).$$
### Primitív függvény[^3]
Adott $f: I\to R$, ahol $I\subset R$. Az $F: I\to R$ függvény $f$ primitívfüggvénye, ha
$$F'(x)=f(x)\quad\quad\forall x\in I.$$
### Határozatlan integrál[^4]
A primitív függvények halmaza a határozatlan integrál.
$$\int{f(x)dx=\{H: I\implies R\quad|\quad H'(x)= f(x)\}}=\{F+c: c\in R\},$$
ahol $F: I\implies R$ tetszőleges primitív függvény.
**Informálisan**:
$$\frac{dF(x)}{dx}=f(x)\quad\quad\Rightarrow\quad\quad dF(x)=f(x)dx$$

[^1]: [[Analízis 1. (2023).pdf#page=130|Analízis 1. Jegyzet 124. oldal]]
[^2]: [[Analízis 1. (2023).pdf#page=127|Analízis 1. Jegyzet 121. oldal]]
[^3]: [[Analízis 1. (2023).pdf#page=134|Analízis 1. Jegyzet 128. oldal]]
[^4]: [[Analízis 1. (2023).pdf#page=135|Analízis 1. Jegyzet 129. oldal]]