---
Óra neve: Matematikai analízis 1.
Előadó: Dr. Vágó Zsuzsanna Márta
Dátum: 2023 Okt. 26.
---
## Folytonosság [^1]
Egy adott $f$ függvény ($f: D \to R$) folytonos, ha minden tetszőleges $x_0$ pontra teljesül, hogy
$$\forall x \in D, \quad |x-x_0| < \delta \quad\Rightarrow\quad |f(x)-f(x_0)| < \varepsilon.$$
**Magyarázásképp**:
Ha a függvény folytonos, minden egymáshoz közeli x értékhez egymáshoz közeli y érték kell hogy tartozzon.
## Sorozatfolytonosság [^2]
Az $f$ függvény [[03 - Számsorozatok 2. és Függvények 1.#Értelmezési tartomány [ 4]|értelmezési tartomány]]ának ($D_f$) egy $x_0$ pontjában sorozatfojtonos, ha $\forall(x_n)\subset D_f$ sorozatra, melyre
$$\lim_{n\to\infty}{x_n}=x_0\text{,}\quad\text{és}$$ $$\lim_{x\to\infty}{f(x_n)}=f(x_0)$$
- Ekvivalens a [[#Folytonosság [ 1]|folytonosság]]gal (bizonyítás az [[Analízis 1. (2023).pdf#page=78|Analízis 1. Jegyzet 72. oldalán]])
## Függvény határérték [^3]
Adott $f$ függvény és $x_0\in R$. Tegyük fel, hogy van olyan $U=(x_0-r, x_0+r)$ környezet, melyre $x_0$ kivételével minden eleme benne van az $f$ függvény értékkészletében. Másszóval:
$$x_0\in R\quad\quad\exists U=(x_0-r,x_0+r)\quad\quad\forall x\in U\backslash\{x_0\}\quad\quad x\in D_f.$$
Az $f$ függvény határértéke $a$, ha minden $\varepsilon$ nagyobb nullánál, és minden $\varepsilon$-hoz létezik $\delta$, ami nagyobb mint nulla, melyekre
$$0<|x-x_0|<\delta,\quad\quad x\in D\Rightarrow|f(x)-a|<\varepsilon$$
$$\lim_{x\to x_0}{f(x)} = a$$
### Baloldali határérték
$f$ baloldali határértéke $x_0$-ban $a\in R$, ha minden $\varepsilon>0$-hoz létezik $\delta>0$, melyre
$$x\in D_f\quad\quad x_0-\delta<x<x_0\Rightarrow |f(x)-a|<\varepsilon.$$
Jelölés:
$$\lim_{x\to x_0^-}{f(x)}=a$$
### Jobboldali határérték
$$x\in D_f\quad\quad x_0<x<x_0-\delta\Rightarrow |f(x)-a|<\varepsilon.$$Jelölés:
$$\lim_{x\to x_0^+}{f(x)}=a$$

[^1]: [[Analízis 1. (2023).pdf#page=76|Analízis 1. Jegyzet 70. oldal]]
[^2]: [[Analízis 1. (2023).pdf#page=78|Analízis 1. Jegyzet 72. oldal]]
[^3]: [[Analízis 1. (2023).pdf#page=80|Analízis 1. Jegyzet 74. oldal]]