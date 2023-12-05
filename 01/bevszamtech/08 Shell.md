---
Óra neve: Bevezetés a számítástechnikába
Előadó: Naszlady Márton Bese
Dátum: 2023 Nov. 22.
---
> [!error] Fontos
>Bash fájl első sorának mindenképpen a következőnek kell lennie, ellenkezőleg nem fut le.
>```sh
>#!/bin/bash
>```

> [!warning] Fontos
> A bash shell szkriptek nem fordítódnak le, ezért nem derül ki előre hogy le tud e majd futni.
### Változók
```sh
VÁLTOZÓ_NEVE="érték"
```

> [!info]
> A változókat ajánlott nagy betűkkel írni.
### Elágazás
```sh
if [[ feltétel ]]
then
	# kód
else
	# kód
fi
```
### While ciklus
```sh
while [[ feltétel ]]
do
	# kód
done
```
### For ciklus
```sh
for i in {1..n}
do
	# kód
done
```
- minden almappa: `i in ./`
- egyes almappák: `i in ./*.txt`
## Komment
```sh
# Shellben a kommentet a Pythonhoz hasonlóan a hash jellel jelöljük.
```
## Parancsok
> [!info]
> Minden működő terminál parancs működő shell sor.