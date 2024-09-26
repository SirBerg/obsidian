<sub class="descriptionSection">25-09-2024 05:27:pm // #Wiki  // [[Programmierung]]</sub>
____
## Ausgabeformatierung
Zum Formatieren von ausgaben in C++ gibt es die library `iomanip`.
Durch diese Library gibt es ein paar funktionen zum ändern von Outputs:
```cpp
setfill(<Zeichen in Hochkommas>) //setz ein Füllzeichen für jede leere Spalte

setw(int n) // setzt die Feldbreite für die nächste Ouput operation

left / right //linksbündige oder rechtsbündige Ausgabe

internal // bei Zahlen: linkes vorzeichen, Wert rechtsbündig
```
### setw Beispiel
Setw ist eine ziemlich confusing function, also dokumentier ich sie hier extra: 
Beispiel für eine normale ausgabe:
```cpp
cout << "Hello World!" << endl
```
Ausgabe:
```text
Hello World
```

Wenn man jetzt setw nutzt:
```cpp
cout << setw(3) << "Hello World" << endl 
```

Jetzt ist die Ausgabe um 3 nach rechts versetzt:
```text
   Hello World
```
### Manipulators für Integers
Für Integers gibt es ein paar extra manipulatoren:
```cpp
dec //dezimale Darstellung (Standard für Int)

hex //hexadezimale Darstellung

oct //oktale Darstellung

showpos /  noshowpos // + bei positiven Zahlen anzeigen oder unterdrücken

uppercase / nouppercase // Groß oder kleinbuchstaben bei Hex Ausgaben (klein = Standard)
```
## Stdin in C++
Um Werte in C++ einzulesen kann die `cin` funktion verwendet werden:
```cpp
cin >> inputVar1 >> inputVar2
```
Falls mehr als eine Input Variable gefordert ist, müssen die Werte per leertaste vom user getrennt werden.
Sobald die C++ executable auf eine cin line stößt wartet es auf input + return taste, somit ist es wichtig das eine Eingabe Aufforderung per cout vorher geschrieben wird, auch wenn mehr als ein Input gefordert ist, sollten die cin calls getrennt werden:
```cpp
cout << "Bitte geben sie ihr gewicht ein:" << endl
cin >> inputVar1
cout << "Bitte geben sie ihr richtiges gewicht ein" << endl
cin >> inputVar2
```