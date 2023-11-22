# Feladatgyűjtemény
<iframe width="100%" height="512px" src="https://users.itk.ppke.hu/~flugi/bevprog_1415/feladatok.html"></iframe>

# 1. Kifejezések
# 2. Vegyes feladatok
# 3. Programozási tételek
## 3.1.cpp
> Számítsd ki egy szám faktoriálisát.
```cpp
# include <iostream>

using namespace std;

int main() {
	int number;
	int counter = 1;
	cin >> number;
	
	int i = 1;
	while (i <= number) {
		counter = counter * i;
		i++;
	}
	
	cout << counter << endl;
	return 0;
}
```
## 3.2.cpp
> Add meg egy természetes szám osztóinak összegét.
```cpp
# include <iostream>

using namespace std;

int main() {
	int counter = 0;
	int n;
	cin >> n;
	
	int i = 2;
	while (i < n) {
		if (n % i == 0) {
			counter += i;
		}
		i++;
	}
	
	cout << counter << endl;
	return 0;
}
```
## 3.3.cpp
> Add meg egy tetszőleges egész szám valódi osztóinak a számát.
```cpp
# include <iostream>

using namespace std;

int main() {
	int counter = 0;
	int n;
	cin >> n;
	
	int i = 2;
	while (i < n) {
		if (n % i == 0) {
			counter++;
		}
		i++;
	}
	
	cout << counter << endl;
	return 0;
}
```
## 3.4.cpp
> Add meg egy természetes szám legnagyobb valódi osztóját.
```cpp
# include <iostream>

using namespace std;

int main() {
	int max = 2;
	int n;
	cin >> n;
	
	int i = 2;
	while (i < n) {
		if (n % i == 0) {
			if (i > max) {
				max = i;
			}
		}
		i++;
	}
	
	cout << max << endl;
	return 0;
}
```
## 3.5.cpp
> Add meg két természetes szám legnagyobb közös osztóját.
```cpp
# include <iostream>

using namespace std;  

int main() {
	int max = 1;
	int n, m;
	cin >> n >> m;
	n = abs(n);
	m = abs(m);
	
	int i = 1;
	while (i <= n and i <= m) {
		if (n % i == 0 and m % i == 0) {
			max = i;
		}
		i++;
	}
	
	cout << max << endl;
	return 0;
}
```
## 3.10.cpp
> Add meg egy tetszőleges egész számsorról, hogy hány eleme kisebb az átlagánál.
```cpp
# include <iostream>
# include <fstream>
# include <string>
# include <vector>

using namespace std;

int main() {
	ifstream file("szamsorozat.txt");
	int sum = 0, average, counter = 0;
	
	if (file.good()) {
		// beolvasás
		vector<int> v;
		while (file.good()) {
			int a;
			file >> a;
			v.push_back(a);
			sum += a;
		}
		file.close();
		
		// átlag
		average = sum / v.size();
		
		int i = 0;
		while (i < v.size()) {
			if (v[i] < average) {
				counter++;
			}
			i++;
		}
		
		cout << counter << endl;
	} else {
		cout << "nem sikerült a beolvasás" << endl;
	}
		
	return 0;
}
```
## 3.11.cpp
> Egy pozitív egész számokból álló számsorban add meg, hogy hány páros szám van.
```cpp
# include <iostream>

using namespace std;

int main() {
	int a, n;
	int counter = 0;
	cin >> n;
	
	int i = 0;
	while (i < n) {
		cin >> a;
		if (a % 2 == 0) {
			counter++;
		}
		i++;
	}
	
	cout << counter << endl;
	return 0;
}
```
## 3.12.cpp
> Egy tetszőleges számsorban add meg a legkisebb és a legnagyobb számot.
```cpp
# include <iostream>

using namespace std;

int main() {
	int n, a;
	int min, max;
	
	cin >> n;
	cin >> a;
	min = a;
	max = a;
	
	int i = 0;
	while (i < n - 1) {
		cin >> a;
		if (a > max) {
			max = a;
		}
		if (a < min) {
			min = a;
		}
		i++;
	}
	
	cout << min << " " << max << endl;
	return 0;
}
```
## 3.13.cpp
> Add meg egy tetszőleges pozitív számsorozat elemeinek a négyzetgyök-összegét.
```cpp
# include <iostream>

using namespace std;

int main() {
	int n, a;
	int counter = 0;
	cin >> n;
	
	int i = 0;
	while (i < n) {
		cin >> a;
		counter += a * a;
		i++;
	}
	
	cout << counter << endl;
	return 0;
}
```
## 3.14.cpp
> Add meg egy tetszőleges pozitív számsorozat elemeinek a négyzetgyök-összegét.
```cpp
# include <iostream>

using namespace std;

int main() {
	int n, c, d, i;
	
	cin >> n;
	int a[n];
	int b[n];
	
	i = 0;
	while (i < n) {
		cin >> c >> d;
		a[i] = c;
		b[i] = d;
		i++;
	}
	
	i = 0, c = 0;
	while (i < n) {
		c += a[i] * b[i];
		i++;
	}
	
	cout << c << endl;
	return 0;
}
```
## 3.15a.cpp és 3.15b.cpp
> a, Egy szigorúan növő egész számsorban add meg a legnagyobb ugrást (szomszédos elemek közötti legnagyobb előforduló különbséget).
> b, Nem monoton számsorra is adj helyes eredményt.
```cpp
# include <iostream>
# include <vector>

using namespace std;

int main() {
	int n;
	cin >> n;
	
	vector<int> sorozat;
	while (sorozat.size() < n) {
		int a;
		cin >> a;
		sorozat.push_back(a);
	}
	
	int max = 0;
	int i = 0;
	while (i < n - 1) {
		if (abs(sorozat[i+1] - sorozat[i]) > max) {
			max = abs(sorozat[i+1] - sorozat[i]);
		}
		i++;
	}
	
	cout << max << endl;
	return 0;
}
```
## 3.16.cpp
>Add meg egy tetszőleges egész számsorban a szomszédos elemek átlagos különbségét.
```cpp
# include <iostream>
# include <vector>

using namespace std;

int main() {
	int n;
	cin >> n;
	
	vector<int> sorozat;
	while (sorozat.size() < n) {
		int a;
		cin >> a;
		sorozat.push_back(a);
	}
	
	int max = 0, sum = 0, i = 0;
	while (i < n - 1) {
		sum += abs(sorozat[i+1] - sorozat[i]);
		i++;
	}
	
	float average = sum / i;
	cout << average << endl;
	return 0;
}
```
## 3.17a.cpp
>Döntsd el három számról, hogy növekvő sorrendben vannak-e.
```cpp
#include <iostream>

using namespace std;

int main() {
	int a, b, c;
	cin >> a >> b >> c;
	if (a < b and a < c and b < c) {
		cout << "igaz"
	} else {
		cout << "hamis"
	}
	
	return 0;
}
```
## 3.17b.cpp
>Tetszőleges sok számról döntsd el ugyanezt.
```cpp
#include <iostream>
#include <string>
#include <vector>

using namespace std;

int main() {
	int n;
	cin >> n;
	
	vector<int> sorozat;
	while (sorozat.size() < n) {
		int a;
		cin >> a;
		sorozat.push_back(a);
	}

	bool nagyobb = true;
	int i = 0;
	while (i < sorozat.size() - 1 and nagyobb) {
		if (sorozat[i] >= sorozat[i+1]) {
			nagyobb = false;
		}
		i++;
	}
	
	if (nagyobb) {
		cout << "a sorozat növekvő" << endl;
	} else {
		cout << "a sorozat csökkenő" << endl;
	}
	return 0;
}
```
## 3.18.cpp
>Add meg egy tetszőleges egész számsorban a prímszámok számát.
```cpp
# include <iostream>
# include <vector>

using namespace std;

bool prim_e(int szam) {
	if (szam == 1) {
		return 0;
	}
	
	int i = 2;
	while (i < szam) {
		if (szam % i == 0) {
			return 0;
		}
		i++;
	}
	return 1;
}

int main() {
	int n;
	cin >> n;
	
	vector<int> sorozat;
	while (sorozat.size() < n) {
		int a;
		cin >> a;
		sorozat.push_back(a);
	}
	
	int counter = 0, i = 0;
	while (i < sorozat.size()) {
		if (prim_e(sorozat[i])) {
			counter++;
		}
		i++;
	}
	
	cout << counter << endl;
	return 0;
}
```
## 3.19.cpp
>Egy egész számról döntsd el, hogy prímszám-e.
```cpp
# include <iostream>
# include <string>

using namespace std;

bool prim_e(int szam) {
	if (szam == 1) {
		return 0;
	}
	
	int i = 2;
	while (i < szam) {
		if (szam % i == 0) {
			return 0;
		}
		i++;
	}
	return 1;
}  

int main() {
	int n;
	cin >> n;
	
	if (prim_e(n)) {
		cout << "igaz" << endl;
	} else {
		cout << "hamis" << endl;
	}
	
	return 0;
}
```
## 3.20.cpp
>a, Sorold fel az első N prímszámot.
>b, Sorold fel a K-nál kisebb prímszámokat.
>c, Sorold fel az A és B közé eső prímszámokat.
```cpp
# include <iostream>
# include <string>

using namespace std;

bool prim_e(int szam) {
	if (szam == 1) {
		return 0;
	}
	
	int i = 2;
	while (i < szam) {
		if (szam % i == 0) {
			return 0;
		}
		i++;
	}
	return 1;
}

void a() {
	int n;
	cin >> n;
	
	int i = 2, counter = 0;
	while (counter != n) {
		if (prim_e(i)) {
			cout << i << " ";
			counter++;
		}
		i++;
	}
}

void b() {
	int k;
	cin >> k;
	
	k--;
	while (k != 0) {
		if (prim_e(k)) {
			cout << k << endl;
		}
		k--;
	}
}

void c() {
	int a, b;
	cin >> a >> b;
	while (a < b) {
		if (prim_e(a)) {
			cout << a << endl;
		}
		a++;
	}
}

int main() {
	a();
	b();
	c();
	
	return 0;
}
```
## 3.21.cpp
>Egy tetszőleges szövegről add meg, hány kis "a" betű van benne.
```cpp
# include <iostream>
# include <string>

using namespace std;

int main() {
	string a;
	cin >> a;
	
	int counter = 0;
	for (char &c: a) {
		if (c == 'a') {
			counter++;
		}
	} 
	
	cout << counter << endl;
	return 0;
}
```
## 3.22.cpp
>Egy tetszőleges szövegről add meg, hány számjegy, hány nagybetű és hány kisbetű van benne.
```cpp
# include <iostream>
# include <string>

using namespace std;

int main() {
	string a;
	cin >> a;
	
	int num = 0, upper = 0, lower = 0;
	for (char &c: a) {
		if (isupper(c)) {
			upper++;
		}
		if (islower(c)) {
			lower++;
		}
		if (isdigit(c)) {
			num++;
		}
	}
	
	cout << num << " " << upper << " " << lower << endl;
	return 0;
}
```
## 3.23.cpp
>Add meg egy tetszőleges szövegben, hogy melyik karakter fordul elő benne a legtöbbször.
```cpp
# include <iostream>
# include <string>

using namespace std;

int main() {
	string a;
	cin >> a;
	
	int maxnum = 1;
	char maxchar = a[0];
	
	int currentnum;
	char currentchar;
	
	for (char i: a) {
		currentchar = i;
		currentnum = 0;
		
		for (char c: a) {
			if (c == i) {
				currentnum++;
			}
		}
		
		if (currentnum > maxnum) {
			maxnum = currentnum;
			maxchar = currentchar;
		}
	}
	
	cout << maxchar << ": " << maxnum << endl;
	return 0;
}
```
## 3.24.cpp
>Add meg egy tetszőleges szövegből a leghosszabb sort.
```cpp
# include <iostream>
# include <string>

using namespace std;

int main() {
	int n;
	cin >> n;
	
	string a;
	getline(cin, a);
	string max = a;
	
	int i = 0;
	while (i < n) {
		getline(cin, a);
		if (a.size() > max.size()) {
			max = a;
		}
		i++;
	}
	
	cout << max << endl;
	return 0;
}
```
## 3.28.cpp
>a, Egy több soros szövegben add meg, hány sorában található meg az "alma" szó.
>b, Az "alma" helyett tetszőleges szöveget lehessen megadni.
>c, A szó összes előfordulásának a számát add meg.
```cpp
# include <iostream>

using namespace std;

int hanyszorbenne(string s, string keresendo) {
	int counter = 0, helper = 0;
	for (char c: s) {
		if (keresendo[helper] == c) {
			helper++;
			if (helper == keresendo.size()) {
				counter++;
				helper = 0;
			}
		} else {
			if (c == keresendo[0]) {
				helper = 1;
			}
		}
	}
	return counter;
}

void a() {
	int n;
	cin >> n;
	
	int counter = 0, i = 0;
	while (i < n + 1) {
		string a;
		getline(cin, a);
		if (hanyszorbenne(a, "alma") != 0) {
			counter++;
		}
		i++;
	}
	cout << counter;
}

void b() {
	string szo;
	int n;
	
	int counter = 0, i = 0;
	while (i < n + 1) {
		string a;
		getline(cin, a);
		if (hanyszorbenne(a, szo) != 0) {
			counter++;
		}
		i++;
	}
	
	cout << counter;
	return 0;
}

void c() {
	string szo;
	int n;
	
	cin >> szo >> n;
	int counter = 0, i = 0;
	while (i < n + 1) {
		string a;
		getline(cin, a);
		counter += hanyszorbenne(a, szo);
		i++;
	}
	
	cout << counter;
	return 0;
}

int main() {
	a();
	b();
	c();
	
	return 0;
}
```
# 4.  Rekordok
## 4.1.cpp
> Adott egy szövegfájl, ami egy recept hozzávalóit tartalmazza. A fájl minden sora egy számmal kezdődik, ami egy összetevőből szükséges mennyiség, majd vesszővel elválsztva tőle az összetevő neve jön.
> a, Add meg azt az összetevőt, amiből a legtöbb, és amiből a legkevesebb kell.
> b, Add meg, hány olyan összetevő van, amiből kevesebb, mint egy egységnyi kell.
> c, Add meg egy tetszőleges összetevőről, hogy mennyi kell belőle.
```cpp
# include <iostream>
# include <fstream>
# include <vector>
# include <string>

using namespace std;
  
struct hozzavalo {
	string nev;
	int mennyiseg;
};

hozzavalo sorbeolvasas(ifstream &f) {
	hozzavalo hozzavalo;
	f >> hozzavalo.mennyiseg >> hozzavalo.nev >> ws;
	getline(f, hozzavalo.nev) >> ws;
	
	return hozzavalo;
}

vector<hozzavalo> beolvasas(ifstream &f) {
	vector<hozzavalo> hozzavalok;
	while (f.good()) {
		hozzavalok.push_back(sorbeolvasas(f));
	}
	return hozzavalok;
}  

void a(vector<hozzavalo> hozzavalok) {
	hozzavalo min, max;
	min = hozzavalok[0];
	max = hozzavalok[0];
	
	int i = 1;
	while (i < hozzavalok.size()) {
		if (hozzavalok[i].mennyiseg < min.mennyiseg) {
			min = hozzavalok[i];
		}
		if (hozzavalok[i].mennyiseg > max.mennyiseg) {
			max = hozzavalok[i];
		}
		i++;
	}

	cout << "min: " << min.nev << " (" << min.mennyiseg << ")" << endl;
	cout << "max: " << max.nev << " (" << max.mennyiseg << ")" << endl;
}

void b(vector<hozzavalo> hozzavalok) {
	int counter = 0, i = 1;
	while (i < hozzavalok.size()) {
		if (hozzavalok[i].mennyiseg < 1) {
			counter++;
		}
		i++;
	}
	
	cout << counter << endl;
}

void c(vector<hozzavalo> hozzavalok) {
	string a;
	cin >> a;
	
	int i = 0;
	while (i < hozzavalok.size()) {
		if (hozzavalok[i].nev == a) {
			cout << hozzavalok[i].mennyiseg << endl;
			return;
		}
		i++;
	}
	
	cout << "nincs ilyen hozzávaló" << endl;
}

int main() {
	ifstream f("hozzavalok.txt");
	if (f.good()) {
		vector<hozzavalo> hozzavalok = beolvasas(f);  
		
		a(hozzavalok);
		b(hozzavalok);
		c(hozzavalok);
	} else {
		cout << "nem sikerült a beolvasás" << endl;
	}
	f.close();
	return 0;
}
```
# 5. Tömbös feladatok
## 5.1.cpp
>Véletlen tömb: egy tömb elemeit töltsd fel véletlen számokkal. _(A következő feladatok akár véletlennel, akár másképp feltöltött vektorokkal foglalkoznak)_
```cpp
# include <iostream>

using namespace std;

int main() {
	int hossz = 4;
	int sorozat[hossz];
	
	int i = 0;
	while (i < hossz) {
		sorozat[i] = rand() % 10 + 1;
		i++;
	}
	
	i = 0;
	while (i < hossz) {
		cout << sorozat[i] << endl;
		i++;
	}
	
	return 0;
}
```
# 6. Függvényes feladatok
## 6.2.cpp
>Valósítsd meg az `int kozos(int a, int b)` függvényt, ami a közös osztók számát adja vissza.
```cpp
using namespace std;

int kozos(int a, int b) {
	int counter = 0, i = 0;
	int minimum;
	
	if (a > b) {
		minimum = b;
	} else {
		minimum = a;
	}

	while (i <= minimum) {
		if (a % i == 0 and b % i == 0) {
			counter++;
		}
		i++;
	}
	
	return counter;
}

int main() {
	return 0;
}
```
## 6.3.cpp
>Valósítsd meg a `bool tokeletes(int a)` függvényt, ami visszaadja, hogy a paraméterül kapott érték tökéletes szám-e.
```cpp
using namespace std;

int osztoosszeg(int a) {
	int i = 1, counter = 0;
	while (i < a) {
		if (a % i == 0) {
			counter += i;
		}
		i++;
	}
	
	return counter;
}

bool tokeletes(int a) {
	return a == osztoosszeg(a);
}

int main() {
	return 0;
}
```
## 6.4.cpp
>Valósítsd meg a `bool baratsagos(int a, int b)` függvényt, ami visszaadja, hogy a paraméterül kapott értékek [barátságos számpárt](http://hu.wikipedia.org/wiki/Bar%C3%A1ts%C3%A1gos_sz%C3%A1mok) alkotnak-e.
```cpp
using namespace std;

int osztoosszeg(int a) {
	int i = 0, counter = 1;
	while (i < a) {
		if (a % i == 0) {
			counter+=i;
		}
		i++;
	}
	
	return counter;
}

bool baratsagos(int a, int b) {
	return osztoosszeg(a) == b and osztoosszeg(b) == a
}

int main() {
	return 0;
}
```
## 6.5.cpp
>Valósítsd meg az int `max(vector<int> v)` függvényt, ami a paraméterül kapott vektor elemei közül a legnagyobbat adja vissza.
```cpp
# include <vector>

using namespace std;

int max(vector<int> v) {
	int max = v[0];  
	int i = 0;
	while (i < v.size()) {
		if (v[i] > max) {
			max = v[i];
		}
		i++;
	}
	
	return max;
}

int main() {
	return 0;
}
```
# 7. Multimédiás feladatok