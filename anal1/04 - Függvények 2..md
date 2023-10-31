---
Óra neve: Matematikai analízis 1.
Előadó: Dr. Vágó Zsuzsanna Márta
Dátum: 2023 Okt. 26.
---
## Folytonosság [^1]
Egy adott $f$ függvény ($f: D \to R$) folytonos, ha minden tetszőleges $x_0$ pontra teljesül, hogy
$$\forall x \in D, \quad |x-x_0| < \delta \quad\Rightarrow\quad |f(x)-f(x_0)| < \epsilon.$$
###### Magyarázásképp:
Ha a függvény folytonos, minden egymáshoz közeli x értékhez egymáshoz közeli y érték kell hogy tartozzon.
## Sorozatfolytonosság [^2]
Az $f$ függvény [[03 - Számsorozatok 2. és Függvények 1.#Értelmezési tartomány [ 4]|értelmezési tartomány]]ának ($D_f$) egy $x_0$ pontjában sorozatfojtonos, ha $\forall(x_n)\subset D_f$ sorozatra, melyre
$$\lim_{n\to\infty}{x_n}=x_0\text{,}\quad\text{és}$$ $$\lim_{x\to\infty}{f(x_n)}=f(x_0)$$
- Ekvivalens a [[#Folytonosság [ 1]|folytonosság]]gal (bizonyítás az [[Analízis 1. (2023).pdf#page=78|Analízis 1. Jegyzet 72. oldalán]])
## Függvény határérték
Adott $f$ függvény és $x_0\in R$. 
$$\lim_{x\to x_0}{f(x)} = a$$
#TODO 
## Külső pont
## Belső pont
#TODO 

[^1]: [[Analízis 1. (2023).pdf#page=76|Analízis 1. Jegyzet 70. oldal]]
[^2]: [[Analízis 1. (2023).pdf#page=76|Analízis 1. Jegyzet 70. oldal]]
