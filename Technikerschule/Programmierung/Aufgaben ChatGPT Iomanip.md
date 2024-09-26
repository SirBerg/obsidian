<sub class="descriptionSection">26-09-2024 02:48:pm // #Übung // [[Programmierung]]</sub>
____
## Aufgabe 1:
### Formatierte Ausgabe von Dezimalzahlen

Schreibe ein Programm, das fünf Dezimalzahlen vom Benutzer einliest und sie mit einer Präzision von zwei Nachkommastellen ausgibt. Verwende `std::fixed` und `std::setprecision` aus der `iomanip`-Bibliothek, um die Zahlen entsprechend zu formatieren.
```cpp
#include <iostream>  
#include <iomanip>  
#include <stack>  
using namespace std;  
int main() {  
    stack<double> s;  
  
    for(int i = 0; i < 5; i++) {  
        cout << "Bitte gib Nummer" << i + 1 << " ein: ";  
        double num;  
        cin >> num;  
        s.push(num);  
    }  
    while(!s.empty()) {  
        cout << fixed << setprecision(2) << s.top() << endl;  
        s.pop();  
    }  
    return 0;  
}
```
## Aufgabe 2:
### Tabellenformatierung

Erstelle ein Programm, das eine Tabelle mit Namen, Alter und Gehalt von 5 Personen ausgibt. Verwende `std::setw` für die Breite der Spalten und `std::left` bzw. `std::right`, um die Ausrichtung der Inhalte in den Spalten zu bestimmen.
```cpp
#include <iostream>  
#include <iomanip>  
#include <stack>  
using namespace std;  
int main() {  
    const string name[] = {"Peter", "Hans", "Helga"};  
    int alter[] = {20, 30, 40};  
    int gehalt[] = {2000, 3000, 4000};  
    cout << left << setw(8) <<"Name" << setw(8) <<"Alter" << setw(8) << "Gehalt" << endl;  
    cout << setfill('-') << setw(24) << "-" << endl;  
    for(int i = 0; i< 3; i++) {  
        cout << setfill(' ') << left << setw(8) << name[i] << setw(8) << alter[i] << setw(8) << gehalt[i] << endl;  
    }  
    return 0;  
}
```
