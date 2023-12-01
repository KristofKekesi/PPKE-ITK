---
Óra neve: Matematikai analízis 1.
Előadó: Dr. Vágó Zsuzsanna Márta
Dátum: 2023 Nov. 16.
---
## Felosztás [^1]
Erre kíváncsi:
$$F=\{x_0=a<x_1<...<x_n=b\}$$

---
$$m_k=\inf\{f(x),\quad x\in[x_{k-1}, x_k]\}$$
$$s_n=\sum_{k=1}^{n}{n_k\Delta x_k}\quad\quad\Delta x_k=x_k-x_{k-1}$$
$$M_k=\sup\{f(x),\quad [x_{k-1}, x_k]\}$$
$$S_n=\sum_{k=1}^{n}{M_k\Delta x_k\quad\quad\Delta x_k=x_k-x_{k-1}}$$
**Állítás**:
$$s_n\leq S_n$$
$$F(\text{valami})=F'$$
$$s_n\leq s'_n\quad\quad S_n\leq S'_n$$
$$\forall F\text{ és }F'$$
$$s(F)\leq S(F')$$
$$\sup s(F)=s\leq\inf S(F)=S$$
### Felosztás finomsága [^2]
A leghosszabb részintervallum hossza:
$$\delta(F)=\max\{x_k-x_{k-1}:k=1,…,n\}.$$
## Előjeles terület, Riemann integrál, Határozott integrál
## Riemann integrálható
$$\text{R}[a,b]=\{f: [a,b]\to R\quad{\text{integrálható}}\}$$
## Riemann összeg [^4]
$$\sigma(F)=\sum_{k=1}^{n}{f(\varepsilon_k)\Delta x_k},$$
ahol $\varepsilon_k\in[x_{k-1},x_k]$ tetszőleges pont az intervallumban. 
## Riemann állandó
## Dirichlet függvény [^6]
## Newton-Leibniz tétel [^3]
Legyen $f: [a,b]\to R$ függvény, tegyük fel,
- korlátos
- integrálható
- $\exists F$ folytonos
- $F'(x)=f(x)\quad\quad\exists x\in(a,b)$
$$\int_{a}^{b}{f(x)dx=F(b)-F(a)}$$
**Jelölés**:
$$\int_a^bf(x)dx=[F(x)]^b_a$$
## Elégséges feltétel integrálásra [^5]
- Ha $f: [a,b]\to R$ folytonos
- Ha $f:[a,b]\to R$ korlátos és monoton
- Ha $f: [a,b]\to R$ korlátos és folytonos, kivéve véges sokszor
## Alaptulajdonságok
**Additív tulajdonság**
$$a<b<c:\quad\quad\int_a^c=\int_a^b+\int_b^c$$
**Lineáris tulajdonság**
$$\int{c\cdot f(x)dx}=c\cdot\int{f(x)dx}$$
**Monoton tulajdonság**
$$\int f'\big(\varphi(x)\big)\cdot\varphi'(x)dx=f\big(\varphi(x)\big)+c\quad\quad c\in R$$

[^1]: [[Analízis 1. (2023).pdf#page=137|Analízis 1. Jegyzet 131. oldal]]
[^2]: [[Analízis 1. (2023).pdf#page=138|Analízis 1. Jegyzet 132. oldal]]
[^3]: [[Analízis 1. (2023).pdf#page=143|Analízis 1. Jegyzet 137. oldal]]
[^4]: [[Analízis 1. (2023).pdf#page=141|Analízis 1. Jegyzet 135. oldal]]
[^5]: [[Analízis 1. (2023).pdf#page=142|Analízis 1. Jegyzet 136. oldal]]
[^5]: [[Analízis 1. (2023).pdf#page=79|Analízis 1. Jegyzet 73. oldal]]