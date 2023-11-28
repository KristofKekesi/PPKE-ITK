# Géptermi ZH feladatok
## 2018.01.16.
#### 2. feladat
A mellékelt NearStars.csv fájl a Naprendszerhez közeli csillagok adatait tartalmazó adatbázis. A fájlban az adatokat ';' választja el egymástól. Az egyes mezők leírása:
```
Common Name - A csillag általános neve  
Sibling - Multi naprendszerek (több csillag van a rendszer középpontjában) esetén a napok kiegészítő betűjele, egyébként üres mező   
Equatorial Coordinates RA - Rektaszcenzió: jobboldali elfordulás az égi egyenlítőn (ekvatoriális koordináta rendszer lambda szöge: óra, perc)  
Equatorial Coordinates DEC - Deklináció: elhajlás az égi egyenlítőtől (ekvatoriális koordináta rendszer phi szöge: fok, fokmásodperc)  
Class - Spektrális osztály, azaz a csillag színkódja  
Visual Magnitude - Látszólagos fényesség (0 hiányzó adatot és nem konkrét értéket jelent!)  
Absolute Magnitude - Abszolút fényesség (10 parsec távolságból észlelt magnitudó)(0 hiányzó adatot és nem konkrét értéket jelent!)  
Parallaxis (Prllx) - Paralaxis (milliívmásodperc) az a szög amely alatt a csillag egy külső pontból (Föld) látszik  
Error - A paralaxis hibája  
Distance (in ligthyear) - A csillag Nap-tól vett távolsága fényévekben  
Gliese - A csillag Gliese kódja   
Other Names/Notes - A csillag egyéb neve jegyzetei  
```
###### Egy kis matek segítség:   
- RA átváltása radiánra: $$\lambda=(\text{óra}+\text{perc}/60)/24360\pi/180$$
- DEC átváltása radiánra:
$$\phi=\text{fok}+\text{fokmásodperc}\cdot60\pi/180$$
Ekvatoriális koordináta rendszerről Descartes koordináta rendszerre áttérés, ahol $R$ a távolság: 
- $X=R\cdot\cos(\phi)\cdot\cos(\lambda)$
- $Y=R\cdot\cos(\phi)\cdot\sin(\lambda)$
- $Z=R\cdot\sin(\phi)$
Két térbeli pont $p_1(x_1,y_1,z_1)$ illetve $p_2(x_2,y_2,z_2)$ távolságának kiszámítása:   
- $D=\sqrt{(x_2-x_1)^2+(y_2-y_1)^2+(z_2-z_1)^2}$
###### A csoport
1. Mekkora a szabad szemmel látható ($\text{Látszólagos fényesség}\leq6$) csillagok átlagos távolsága a Földtől? (Az adat nélküli törpe csillagokat nem számítva)
2. Melyik a második leggyakoribb csillag szín kód? 
3. Melyik két csillag van a legtávolabb egymástól az adatbázisban szereplők közül?
###### B csoport
1. Add meg külön-külön, hogy az egyes multi nap rendszerekből hány található az adatbázisban!  
    _Hány darab bináris naprendszer, hány darab trináris naprendszer stb._
2. Határozd meg az adatbázison a relatív paralaxis hiba átlagát! Értelemszerűen a Napot (Sun) ne számold bele! (Relatív paralaxis hiba: paralaxis hiba/paralaxis*100)   
    Majd az átlagnál pontosabb mérési eredményekkel bíró csillagok közül határozd meg a legtávolabbit!
3. Határozd meg azt a csillag párt, melyek a legtávolabb esnek egymástól!
## 2017.12.19. 
#### 2. feladat
A mellékelt movies_tmdb.txt fájl egy filmeket tartalmazó adatbázis. A fájl az alábbi formátumot követi:
```
id;original_title;genres;original_language;budget;production_companies;production_countries;release_date;runtime;revenue;title;vote_average;vote_count
```
**Azaz**:  
azonosító; az eredeti cím; a műfaji besorolások; eredeti nyelv; költségvetés; gyártásért felelős cégek; gyártásban szerepet játszó országok; megjelenés dátuma (YYYY-MM-DD); film hossza (perc); bevétel; cím; szavazati átlag pontja, szavazók száma 
**Tippek**: 
1. A fáljban ";"-ők választják el az egyes mezőket
2. A "genres", "production_companies", "production_countries" adatok igazából ", "-vel elválaszott listák, hisz egy filmnek több műfaja, gyártó cége, illetve gyártásban szerepet játszó országa is lehet
3. A "budget", "revenue" mezők nagyon-nagy számokat (milliós, milliárdos) tartalmaznak, ezt tartsd szem előtt!
###### A csoport délelőtt
1. Melyik a 2010-es év legjobb filmje a szavazati átlag pontok alapján?
2. Az egész adatbázis tekintve mennyi lesz egy filmek a cégenkénti átlagos nyeresége?   
    _(céges nyereség: (bevétel-költségvetés)/filmhez tartozó cégek száma) Fontos: Amelyik filmnél nincs feltüntetve cég az nem számít bele az átlagba! (Hagyd ki!)_
3. Mely filmes műfaj a leggyakoribb?
###### B csoport délelőtt
1. Melyik a Walt Disney Pictures leghosszabb filmje?
2. Sorold fel azokat a filmket, melyek a legtöbb gyártásban szerepet játszó országgal rendelkeznek!
3. Melyik a legsikeresebb filmes év?   
    _(Azaz melyik évben a legnagyobb a megjelent filmek pontjainak összege?)_
###### A csoport délután
1. Mikor jelent meg a legrégebbi SciFi (Science Fiction) film? _(elég csak az évet vizsgálni)_
2. Mely filmek kapták a legtöbb műfaj besorolást?
3. Az angol nyelvet nem számítva melyik eredeti filmes nyelv a legelterjedtebb? _(elég a betűjele)_
###### B csoport délután
1. A szavazatot kapott filmek közül, hány darab filmnek van átlagon felüli szavazója?   
    _(Azaz a szavazóinak a száma az átlag szavazó szám fölött van.)_
2. Melyik az a film, ahol a cégekre lebontott nyereség a legtöbb?   
    _(céges nyereség: (bevétel-költségvetés)/filmhez tartozó cégek száma)_
3. Add meg a legtöbb filmet jegyző céget!   
    _Fontos: Csak azokat a filmeket számold, ahol meg van adva cég!_