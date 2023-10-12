# Adattárolás
### Volatilis (Volatile)
Folyamatos energia kell a tároláshoz. Ha nincs áram sérül az adat.
Pl.: emberek, RAM

### Nem volatilis (Nonvolatile)
Nincs kell folyamatos energiaigénye.
Pl: CD

## Memóriák
### Dinamikus memória
Folyamatosan frissíteni kell a tárolt értéket.
### Statikus memória
Nem kell állandóan frissíteni a tárolt értéket.

### Read-Only Memory (ROM)
- Programmable ROM: egyetlen alkalommal programozható, speciális eszközzel
- EPROM: UV fénnyel lehet törölni, majd újra írni
- EEPROM: Elektronikusan újraírható

### Random Access Memory (RAM)
Minden címet ugyanannyi idő elérni.

# Memória-hierarchia
A gyors memóriák kicsik és drágák, ezért többfélét kell használni.
```
           /\
          /  \
         /    \
        / CPU  \ 
       /        \
      / Register \
     / L1 Cache   \
    / L2 Cache     \
   / L3 Cache       \
  / RAM              \
 / HDD, SSD           \
/ Cloud                \
```

## Merevlemez (HDD)
- keresési idő: lemez mozgási ideje + olvasási idő
### CHS Adressing
- Cilinderesen van felosztva a lemez
### LBA Adressing
- Spirálirányű felbontása a lemeznek

## Partícionálás
### Redundant Array of Independent (Inexpensive) Disks (RAID)
#### RAID 0
- semennyire nem redundáns
#### RAID 1
- minden fájl megtalálható minden lemezen
#### RAID 10
- RAID 1 és RAID 0 ötvözve
#### RAID 5
- a paritás elosztva van minden lemezen

# Fájlrendszerek
- Metaadatok tárolását is lehetővé teszi
	- tulajdonosa
	- módosítás dátuma
	- jogosultságok

### New Technology File System (NTFS)
- max fájlméret 256TB
- jogosultságok
- megbízható
- Windows

### Ext4
- max fájlméret 16TB
- Linux
- könnyű managelhetőség

### File Allocation Table (FAT)
- max fájlméret 4BG
- egyszerű, jól támogatott fájlrendszer

## Töredezettség
### Külső töredezettség
- részekre szedhetjük a fájlokat
### Belső töredezettség
- megadott 4KB-os slot-ok vannak

# Adatkommunikáció
### Párhuzamos adatátvitel
- annyi szál ahány bit
- egyszerre fut -> gyors
Pl: CPU és Memória között

### Soros átvitel
- kisebb helyigény
- lassabb
## Buszok

## Aszinkron kommunikáció
- feedback
## Szinkron kommunikáció
- clock