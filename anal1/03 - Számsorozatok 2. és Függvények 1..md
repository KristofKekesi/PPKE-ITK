---
Óra neve: Matematikai analízis 1.
Előadó: Dr. Vágó Zsuzsanna Márta
Dátum: 2023 Okt. 12.
---
## Konvergens [^1]
Ha tart valahova, A határértéke. 
$|a_n-A| < \epsilon$, $\forall n > N$. Másként leírva $\lim_{n\to \infty}a_n = A$
## Divergens [^1]
Ha nem konvergens.
## Határérték [^1]
A sorozat ha konvergens, van határértéke, ez az A.
$|a_n - A| < \epsilon$, $\forall \epsilon > N$. Másképp kifejezve: $\lim_{n\to \infty}{a_n} = A$
## Rekurzív sorozat [^2]
Olyan sorozat aminek a képletében hivatkozunk egy a sorozat másik elemére.
## Torlódási pont [^3]
$t$ akkor torlódási pontja a sorozatnak, ha a $t$ pont [[01 - Valós számok bevezetése#Környezet|környezet]]ében a sor végtelen sok eleme található meg. Vagyis  a $(t-\epsilon; t + \epsilon)$ intervallumon belül ($\epsilon > 0$), végtelen sok eleme van a sornak. 
# Függvények
## X, Y halmazok [^4]
Adott két halmaz (X, Y) ezek között fennáll egy $f: X \to Y$ leképezés. $x\in X$ hozzárendelünk egyetlen y elemet az Y halmazból. Ezt így jelöljük:
$$f(x) = y$$
$$x \rightarrow y$$
## Injektív [^4]
Ha $f(x_1) ≠ f(x_2)$ bármilyen $x_1,x_2\in X$ esetén ("Nincs két azonos y").
## Szürjektív [^4]
Ha minden $y\in Y$-hoz létezik x, amely $f(x) = y$. ("Nincs két azonos x")
## Bijektív [^5]
Ha a függvény [[03 - Számsorozatok 2. és Függvények 1.#Injektív|injektív]], és [[03 - Számsorozatok 2. és Függvények 1.#Szürjektív|szürjektív]] is, ilyenkor a függvény kölcsönösen egyértelmű az X és Y halmazok között.
## Inverz függvény [^1]
Ha a függvény [[03 - Számsorozatok 2. és Függvények 1.#Bijektív|bijektív]], akkor létezik inverz függvénye:
$$f^{-1}: Y \to X$$ melyre:
$$f^{-1}(f(x))=x$$
$$f^{-1}(f(y))=y$$
## Összetett függvény [^5]
Adott két függvény. Ezek $f:X \to Y$ és $g: Y \to Z$. Az összetett függvény $X \to Z$ típusú hozzárendelés, vagyis $g(f(x))$.
## Értelmezési tartomány [^4]
Jele: D<sub>f</sub> (az angol DOMAIN szóból)
## Értékkészlet [^4]
$\forall y \in Y$ amely megjelenik képként, vagyis $$D_f = \{y\in Y: \exists x \in X, f(x) = y\}$$
Jele: R<sub>f</sub> (az angol RANGE szóból)
## Függvény gráfja [^5]
$$\{x, f(x) : x\in D\} \subset R^2$$

[^1]: [[Analízis 1. (2023).pdf#page=33|Analízis 1. Jegyzet: 27. oldal]]
[^2]: [[Analízis 1. (2023).pdf#page=39|Analízis 1. Jegyzet: 33. oldal]]
[^3]: [[Analízis 1. (2023).pdf#page=50|Analízis 1. Jegyzet: 44. oldal]]
[^4]: [[Analízis 1. (2023).pdf#page=70|Analízis 1. Jegyzet: 64. oldal]]
[^5]: [[Analízis 1. (2023).pdf#page=71|Analízis 1. Jegyzet: 65. oldal]]