---
Óra neve: Matematikai analízis 1.
Előadó: Dr. Vágó Zsuzsanna Márta
Dátum: 2023 Nov. 06.
---
## Szinusz függvény[^1]
## Cosinus függvény[^1]
## Érintő egyese
Legyen $x_0$ az $f$ függvény értelmezési tartományának belső pontja, itt differenciálható. Ekkor a függvény $x_0$ pontjához tartozó érintő egyenese
$$x_0\in D_f\quad\quad y_0=f(x_0)\quad\quad m=f'(x_0)$$
$$y-y_0=m(x-x_0)\quad\Rightarrow\quad y=m(x-x_0)+y_0.$$
## Lokális szélsőértékek [^3]
### Lokális minimum
Ha $x_0$-nak legalább egy környezete van, amelyre
$$f(x)\ge f(x_0)\quad\quad\forall x\in U\cap D_f.$$
### Lokális maximum
Ha $x_0$-nak legalább egy környezete van, amelyre
$$f(x_0)\ge f(x)\quad\quad\forall x\in U\cap D_f.$$
### Elégséges feltétel lokális szélsőértékre
Legyen $f: D_f\to R$, $x_0$-ban kétszer folytonosan differenciálható, és $f'(x)=0$. Ekkor $f''(x_0)≠0$ esetén $x_0$-ban lokális szélsőérték van. Sőt,
$$f''(x_0)>0\quad\quad\ x_0\text{ lokális minimum}$$
$$f''(x_0)<0\quad\quad\ x_0\text{ lokális maximum}$$
> [!info]
> Ha $f''(x)=0$, még nem eldönthető, vajon $x_0$-ban szélsőértéke van-e a függvénynek. (Innen az elégséges)
### Szükséges feltétel lokális szélsőértékre
Legyen $f: D_f\to R$, $x_0$-ban differenciálható. Ekkor
$$f'(x)=0.$$
## Globális szélsőértékek [^4]
### Globális minimum
$$f(x)\ge f(x_0)\quad\quad\forall x\in D_f$$
### Globális maximum
$$f(x_0)\ge f(x)\quad\quad\forall x\in D_f$$
## Magasabb rendű deriváltak [^5]
### Másodrendű derivált
Ha egy $f$ függvény deriválható $x_0$ egy környezetében, és ez az $f'$ függvény deriválható $x_0$-ban, akkor ez az $f$ függvény másodrendű deriváltja.
$$f''(x)=\lim_{x\to x_0}{\frac{f'(x)-f'(x_0)}{x-x_0}}$$
### N-ed rendű derivált
$$\text{Jelölése:}\quad f^{(n)}(x)$$
## Stacionárius pont [^4]
Minden olyan $x_0\in D_f$ szám stacionárius pont amelynek derivált értéke $0$.
$$f'(x_0)=0\quad\quad x_0\in D_f$$
## Középérték tételek [^6]
### Rolle tétel
Legyen $f: [a, b]\to R$. Tegyük fel, hogy $f$
- folytonos $[a,b]$-n, és differenciálható $(a,b)$-n
- $f(a)=f(b)$
$$\exists\varepsilon\in(a,b)\quad\quad f'(\varepsilon)=0$$
**Másképpen**:
Ha egy függvény folytonos, és két helyen is felveszi ugyan azt az értékét lesz $\varepsilon$ pontja, ahol a deriváltja $0$ lesz ([[06 - Függvények 4.#Stacionárius pont [ 4]|Stacionárius pont]]).
![[rolle.png]]
### Lagrange-féle középérték tétel
Legyen $f: [a,b]\to R$. Tegyük fel, hogy $f$
- folytonos $[a,b]$-n, és differenciálható $(a,b)$-n
$$\exists\varepsilon\in(a,b)\quad\quad f'(\varepsilon)=\frac{f(b)-f(a)}{b-a}.$$
![[lagrange.png]]
## Inverz függvény deriváltja [^7]
Tegyük fel, hogy $f$ szigorúan monoton, differenciálható függvény, melyre $f'(x)≠0, x\in D_f$ mellett. Ekkor $f^{-1}$ is differenciálható, és
$$(f^{-1})(y)=\frac{1}{f'(f^{-1}(y))}.$$

[^1]: [[Analízis 1. (2023).pdf#page=74|Analízis 1. Jegyzet 68. oldal]]
[^3]: [[Analízis 1. (2023).pdf#page=123|Analízis 1. Jegyzet 117. oldal]]
[^4]: [[Analízis 1. (2023).pdf#page=124|Analízis 1. Jegyzet 118. oldal]]
[^5]: [[Analízis 1. (2023).pdf#page=120|Analízis 1. Jegyzet 114. oldal]]
[^6]: [[Analízis 1. (2023).pdf#page=125|Analízis 1. Jegyzet 119. oldal]]
[^7]: [[Analízis 1. (2023).pdf#page=121|Analízis 1. Jegyzet 115. oldal]]