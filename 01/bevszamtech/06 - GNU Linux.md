---
Óra neve: Bevezetés a számítástechnikába
Előadó: Naszlady Márton Bese
Dátum: 2023 Nov. 08.
---
# Operációs rendszer
**Céljai**:
- kényelmesen használható felületet ad
- elrejti a hardware körülményességeit
- okosan használja az erőforrásokat
- egységesített környezet a programok számára
## Kernel
Közvetlen kapcsolat a hardware-rel. Kezeli a
- memóriát
- futó programokat
- fájlrendszert
## Shell
- GUI és CLI és egyéb lehetőségek (Siri, taktilis kijelzés, játékgép)
- Kezeli a környezeti paramétereket (qwertz és qwerty, ...)
# GNU projekt
- a program szabadon használható mindenre
- a program szabadon módosítható
- a program tovább adható ingyen, pénzért
# Linux
GNU + Linux -> GNU/Linux -> Linux
![](https://upload.wikimedia.org/wikipedia/commons/1/1b/Linux_Distribution_Timeline.svg)
## Fájl struktúra
```
. /
|__ bin/
|__ etc/
|__ opt/
|__ tmp/
|__ usr/
	|__ bin/
	|__ man/
	|__ lib/
	|__ local/
	|__ share/
|__ var/
	|__ log/
	|__ tmp/
	|__ lock/
|__ home/
|__ temp/
```
### Abszolút elérési út
Elérési út a gyökérből kezdődően.
```
/home/kekkr/public_html/
```
### Relatív elérési út
A jelenlegi "working directory"-ból kezdődően az elérési út.
- Jelenlegi mappa: `./`
- Visszalépés: `../`
```
../../fish.txt
```
## Jogosultságok
Öröklődnek a fa struktúrában a jogosultságok.
- Olvasás (r, 1, 001)
- Írás (w, 2, 010)
- Futtatás (x, 3, 100)
### Csoportok
Minden 
- Tulajdonos: akié az adott fájl
- Csoport: amelyik csoporthoz tartozik a fájl
- Más: e fentiek közül egyik se
```c
drwxrwxrwx
- típus
	- l: link
	- d: mappa
	- -: fájl
 --- tulajdonos jogosultságai
    --- csoport jogosultságai
       --- más jogosultságai
```
## Linkek
### Hard link
- Meghajtón lévő adatra mutat
### Soft link
- [[#Hard link]]re mutat
## Csatlakozás szerverhez
[[SSH segédlet.pdf]]
[[Szerverek]]
## Alap parancsok
### Copy (`cp`)
```shell
cp honnan hova
```
### Manual (`man`)
```shell
man parancs_neve
```
### Make directory (`mkdir`)
```shell
mkdir uj_mappa_neve
```
### Remove directory (`rmdir`)
```shell
rmdir mappa_neve
```
### Change directory (`cd`)
```shell
cd eleresi_ut
```
### Print working directory (`pwd`)
```shell
pwd
```
### Jogosultság lekérdezése
```shell
ls -l
```
- Itt sorba látjuk a fájlokat, vele együtt a jogosultságokat.
### Jogosultság módosítása (`chmod`)
```shell
chmod 777
```
- Első számjegy: Tulajdonos
- Második számjegy: Csoport
- Harmadik számjegy: Más
### Link készítése
```shell
ln -s eleresi_ut
```
## Git parancsok
![[09 Verziókezelés#Git CLI (Git Command Line Interface)]]
## Összetett műveletek
### Joker karakterek
- `*`: Bármennyi bármilyen karakterrel helyettesíthető
- `?`: Kérdőjelenként bármilyen karakterrel helyettesíthető
- `[a,b,c]`: A zárójelen belülről bármelyik karakterrel helyettesíthető
```shell
ls *.txt
find -name "???"
```
### Kiírás fájlba
Minden ami a terminálba menne ki a fájlba fogja írni.
```sh
parancs >> fájl_neve
```
Kiírás fájlba, de **töröl minden eddigit a fájlból**.
```sh
parancs > fájl_neve
```
## Bemenet fájlból
A program egy fájt használ bemenetként a terminál helyett.
```sh
parancs < fájl_neve
```
## Kimenet átadása másik programnak
Az első program kimenetét használja a második inputnak.
```sh
első | második
```
## Hibaüzenetek eltüntetése
```sh
parancs>/dev/null
```