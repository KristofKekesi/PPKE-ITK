---
Óra neve: Matematikai analízis 1.
Előadó: Dr. Vágó Zsuzsanna Márta
Dátum: 2023 Okt. 30.
---
## [[04 - Függvények 2.#Folytonosság [ 1]|Folytonosság]]
## Szakadás [^1]
Ha $f$ függvény az értelmezési tartomány egy $x_0$ pontjában nem folytonos, akkor ott **szakadási hely**e van. Ezen kívül $x_0\notin D_f$, akkor is szakadási hely, ha
$$(x_0-\delta, x_0+\delta)\backslash\{x_0\}\subset D_f\quad\quad\delta>0.$$
Vagyis: Ha egy $x_0$ [[01 - Valós számok bevezetése#Környezet|környezetében]], amiből kivesszük az $x_0$-t, eleme a függvény [[03 - Számsorozatok 2. és Függvények 1.#Értékkészlet [ 4]|értékkészlet]]ének akkor szakadási pont.
### Osztályozásuk:
- #### Elsőfajú szakadás
	$x_0$-ban elsőfajú szakadás van, ha létezik a függvénynek az $x_0$-ba tartó baloldali, és jobboldali határértékei és ezek kisebbek, mint végtelen.
	Megszüntethető szakadás, ha a két oldalsó szélsőérték megegyezik, és
	$$\lim_{x\to x_0}{f(x)≠f(x)}.$$
- #### Másodfajú szakadás
	Ha nem elsőfajú.
## Bolzano tétel [^2]
Adott $f: [a,b]\to R$ folytonos függvény. Tegyük fel, hogy $f(a)\leq0\leq f(b)$. Ekkor $\exists\epsilon\in(a, b)$ , ahol $f(\epsilon)=0$.

Másképpen:
Ha van egy folytonos zárt függvényem aminek az egyik vége negatív, a másik pozitív, akkor biztosan lesz olyan pontja amely nulla.
## Inverz függvény folytonossága [^2]
Adott $f$ függvény, amely $f:[a, b]\to R$, szigorúan monoton növekvő, folytonos.
$$c\in[f(a), f(b)]\quad\quad\mathcal{E}\in[a, b]$$
Az inverz függvény a $c\to\mathcal{E}$ leképezés.
## Weierstrass I. tétele [^3]
Legyen $f: [a, b]\to R$ függvény folytonos.
**Ekkor az $f$ függvény korlátos.**
## Weierstrass II. tétele [^3]
Legyen $f: [a, b]\to R$ függvény folytonos.
**Ekkor az $f$ függvény felveszi a minimumát és a maximumát $[a, b]$-ben.**
## Nevezetes határértékek [^4]
$$\lim_{x\to0}{\frac{\sin x}{x}}=1$$
$$\lim_{x\to0}{\frac{1-\cos x}{x^2}}=\frac{1}{2}$$
$$\lim_{x\to\infty}{x^{\frac{1}{x}}}=1$$
# Differenciálszámítás
## Differenciálhányados [^5]
Adott $f$ függvény, és $x_0\in \text{int}D$. Az $x$ ponthoz tartozó differenciálhányados a szelő meredeksége.
$$\frac{f(x)-f(x_0)}{x-x_0},\quad\quad x\in D_f$$
## Derivált
A differenciálhányados határértéke a derivált.
$$f(x)'=\lim_{x\to x_0}{\frac{f(x)-f(x_0)}{x-x_0}}=\frac{df}{dx}(x_0)$$
## Deriválási szabályok
$$(f+g)'(x_0)=f'(x_0)+g'(x_0)$$
$$(f\cdot g)'(x_0)=f'(x_0)\cdot g(x_0)+f(x_0)\cdot g'(x_0)$$

[^1]: [[Analízis 1. (2023).pdf#page=91|Analízis 1. Jegyzet 85. oldal]]
[^2]: [[Analízis 1. (2023).pdf#page=95|Analízis 1. Jegyzet 89. oldal]]
[^3]: [[Analízis 1. (2023).pdf#page=100|Analízis 1. Jegyzet 94. oldal]]
[^4]: [[Analízis 1. (2023).pdf#page=101|Analízis 1. Jegyzet 95. oldal]]
[^5]: [[Analízis 1. (2023).pdf#page=110|Analízis 1. Jegyzet 104. oldal]]