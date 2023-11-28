---
Óra neve: Matematikai analízis 1.
Előadó: Dr. Vágó Zsuzsanna Márta
Dátum: 2023 Nov. 20.
---
## Határozott integrál
## Számtani közép
$$A=\frac{\sum_{k=1}^{n}{a_k}}{n}=\frac{\sum_{k=1}^{n}{a_k}}{\sum_{k=1}^{n}{1}}$$
## Integrálközép [^2]
Jele: $\kappa\quad\text{(kappa)}$
Adott $f:[a,b]\to R$  integrálható függvénynek az integrálközepe $\kappa$ szám, ha
$$\kappa=\frac{\int_a^b{f(x)dx}}{b-a}.$$
**Állítás**:
Tegyük fel, $m\leq f(x)\leq M\quad\forall x$. Ekkor $m\leq\kappa\leq M$.
**Következmény**:
Tegyük fel, $f$ folytonos. Ekkor $\exists\epsilon\in(a,b)\quad f(\epsilon)=\kappa$.
## Parciális integrálás [^3]
Legyenek $f,g:[a,b]\to R$, integrálható függvények.
#### Határozatlan integrálás
$$\int{f'(x)g(x)}dx=f(x)g(x)-\int{f(x)g'(x)}dx$$
#### Határozott integrálás
$$\int_a^b{f'(x)g(x)}dx=\bigg[f(x)g(x)\bigg]_a^b-\int_a^b{f(x)g'(x)}dx$$
## Helyettesítés [^1]
$$\int_a^b{f(x)}dx=\int_a^b{f(\phi)}d\phi$$
**Informálisan**: $d\phi(t)=\phi'(t)dt$
#### Helyettesítés integrálban [^1]
$f:[a,b]\to R$ integrálható
$\phi:[\alpha,\beta]\to[a,b]$ differenciálható, szigorúan monoton
**Ekkor**:
$$\int_a^b{f(x)}dx=\int_\alpha^\beta{f\big(\phi(t)\big)\phi'(t)}dt$$
## Lokálisan integrálható
$$A(t)=\int_1^t{\frac{1}{x^2}}=\bigg[\frac{x^{-1}}{-1}\bigg]=\frac{t^{-1}}{-1}-\frac{1}{-1}=1-\frac{1}{t}$$

$$\int_1^\infty{\frac{1}{x}}dx=1$$

[^1]: [[Analízis 1. (2023).pdf#page=152|Analízis 1. Jegyzet 146. oldal]]
[^2]: [[Analízis 1. (2023).pdf#page=147|Analízis 1. Jegyzet 141. oldal]]
[^3]: [[Analízis 1. (2023).pdf#page=148|Analízis 1. Jegyzet 142. oldal]]