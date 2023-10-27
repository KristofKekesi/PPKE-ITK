```cpp
#include <fstream> /* Fejállomány */

int main() {
	int variable;
	
	ifstream input_file_stream("filename.txt"); /* Befájl */
	ofstream output_file_stream; /* Kifájl */
	
	/* Ajánlott: megnézni hogy sikerült e a beolvasás */
	if (!input_file_stream.good()) {
		cout << 0
	}
	
	input_file_stream.good() /* Olvasható-e még */
	input_file_stream >> variable /* Olvasás fájlból */
	input_file_stream.close(); /* Fájl bezárása */
}
```
- léteznie kell a beolvasandó fájloknak