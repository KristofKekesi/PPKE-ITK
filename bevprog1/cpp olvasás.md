## Fejállomány
```cpp
#include <fstream> /* Fejállomány */
```
## Típusok
- ifstream ('Input File Stream'): fájlbeolvasás
```cpp
ifstream valtozonev_in("filename.txt"); /* Befájl */
```
- ofstream ('Output File Stream'): fájlba írás
```cpp
ofstream valtozonev_out; /* Kifájl */
```
## Olvasás
```cpp
ifstream valtozonev_in("filename.txt"); /* Befájl */

/* Ajánlott: megnézni hogy sikerült e a beolvasás */
if (!valtozonev_in.good()) {
	valtozonev_in >> variable; /* Olvasás fájlból */
}

valtozonev_in.close(); /* Fájl bezárása */
```
- léteznie kell a beolvasandó fájloknak
### Egész sor beolvasása
```cpp
getline(valtozonev_in, variable);
```
- használható a terminálon is
#todo 
ws