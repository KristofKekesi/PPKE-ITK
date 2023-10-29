---
Óra neve: Bevezetés a számítástechnikába
Előadó: Naszlady Márton Bese
Dátum: 2023 Okt. 25.
---
# Preambulum
A LaTeX dokumentum `\begin{document}` előtti része. Általában globális paramétereit tudjuk beállítani.
Példa a preambulumra:
```latex
\documentclass[a4paper]{article}
\usepackage[utf8]{inputenc} \usepackage[magyar]{babel} \usepackage{amsmath} %matematikai modul
\usepackage[pdftex,unicode,raiselinks,colorlinks]{hyperref} %működő linkek
\usepackage[magyar]{babel} %magyar nyelv beállítása

\title{cím}
\author{szerző neve}
\date{\today} % a \today paranccsal a fordítás napját helyettesíti be
```
# Matematikai kifejezések
Minden Obszidián-ban használható matematikai kifejezés működő LaTeX kifejezés.
Hasznos editor: [[https://latex.codecogs.com/eqneditor/editor.php||Codecogs LaTeX editor]]
## Környezetek
### Sorközi  kifejezés
Az Obsidian-ban is működik a `$<kifejezés>$`.
### Sorkihagyásos  kifejezés
Az Obszidián-ban is működik a `$$<kifejezés>$$`.
### Sorkihagyásos kifejezés
```latex
\begin{equation}
<kifejezés>
\end{equation}
```
## Szimbólumok
- kihagyás: `\quad` $a \quad b$
- végtelen: `\infty` $\infty$
- hasonlóság: `\sim` $\sim$
- szorzás jel: `\cdot` $\cdot$
# Hasznos dokumentumok
- [[Csárdi Gábor - LaTeX nem túl röviden.pdf]]
- [[LaTeX puska.pdf]]