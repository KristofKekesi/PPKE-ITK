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
> Add meg egy tetszőleges egész számsorban a szomszédos elemek átlagos különbségét.
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
> Döntsd el három számról, hogy növekvő sorrendben vannak-e.
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
> Tetszőleges sok számról döntsd el ugyanezt.
```cpp
```
# 4.  Rekordok
# 5. Tömbös feladatok
# 6. Függvényes feladatok
# 7. Multimédiás feladatok