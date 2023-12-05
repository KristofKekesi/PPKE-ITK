---
Óra neve: Bevezetés a számítástechnikába
Előadó: Naszlady Márton Bese
Dátum: 2023 Nov. 29.
---
## Verziókezelő rendszerek
- CVS (Concurrent Version System)
- Git
### Centralized Version Control System
**Például**: SVN
### Distributed Version Control System
**Például**: Git
## Git szerverek
- [GitHub](https://www.guthib.com)
- GitLab ([dev.itk.ppke.hu](https://www.dev.itk.ppke.hu))
- BitBucket
## Verzió
- Revision number
- Név
- Leírás
- …
# Git CLI (Git Command Line Interface)
Git repó klónozása.
```sh
git clone eleresi_ut
```
Repó naprakészre frissítése.
```sh
git pull
```
Minden fájl hozzáadása a githez.
```sh
git add .
git add *
```
Módosítások mentése.
```sh
git commit -m "commit message"
```
Módosítások közzététele.
```sh
git push
```
Ág összeolvasztása.
```sh
git merge
```