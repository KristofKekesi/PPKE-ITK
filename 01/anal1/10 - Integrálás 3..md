---
Óra neve: Matematikai analízis 1.
Előadó: Dr. Vágó Zsuzsanna Márta
Dátum: 2023 Nov. 23.
---
## Integrálfüggvény [^3]
Legyen $f: [a,b]\to R$ integrálható függvény. Ekkor az $f$ függvény integrálfüggvényét így definiáljuk:
$$F(x)=\int_a^x{f(t)}dt$$
**Állítás**:
- $F$ folytonos $[a,b]$-n,
- Ha $f$ folytonos az $x_0\in(a,b)$ pont egy környezetében, akkor $x_0$-ban $F$ differenciálható, és
- $F'(x_0)=f(x_0)$
#todo
$$\frac{d}{dx}\bigg(\int_a^x{f(t)}dt\bigg)$$
**Bizonyítás**:
[[09 - Integrálás 2.#Integrálközép [ 2]|Integrálközép]] alapján.
## Lokálisan integrálható [^4]
Az $f$ függvény lokálisan integrálható $I$-ben, ha minden $[a,b]\subset I$ korlátos és zárt intervallum esetén $f|_{[a,b]}$ integrálható. Ezt így jelöljük:
$$f\in R^{\text{loc}}(I).$$
# Improprius integrál [^1]
Valami nem stimmel, nem proper.
$f$ inpropriusan integrálható, ha $\exists A(t)=I$
$$\int_a^\infty{f(x)dx}=\lim_{t\to\infty}{\int_a^\infty{f(x)}dx}$$
Ha $f:(-\infty, a]\to R$, akkor
$$\int_{-\infty}^a{f(x)}dx=\lim_{t\to-\infty}{B(t)}$$
#todo 2 esete van
## 1. eset
## 2. eset
$R_f$ végtelen.
## Majoráns kritérium [^2]
Adottak $f,g:[a,\infty)\to R$ lokálisan integrálható függvények. Tegyük fel, $0\leq|f(x)|\leq g(x)\quad \forall x\in[a,\infty).$
$$\int_a^\infty{g(x)}dx<\infty\quad\Rightarrow\quad\int_a^\infty{f(x)}dx<\infty$$
## Minoráns kritérium [^2]
Adottak $f,g:(\alpha,\beta)\to R$ függvények. Tegyük fel, hogy $f(x)\leq g(x)\quad\forall x\in(\alpha, \beta)$.
$$\int_\alpha^\beta{f(x)}dx=\infty\quad\Rightarrow\quad\int_\alpha^\beta{g(x)}dx=\infty$$

[^1]: [[Analízis 1. (2023).pdf#page=155|Analízis 1. Jegyzet 149. oldal]]
[^2]: [[Analízis 1. (2023).pdf#page=160|Analízis 1. Jegyzet 154. oldal]]
[^3]: [[Analízis 1. (2023).pdf#page=153|Analízis 1. Jegyzet 147. oldal]]
[^4]: [[Analízis 1. (2023).pdf#page=156|Analízis 1. Jegyzet 150. oldal]]