<sub class="descriptionSection">20-09-2024 10:41:am // #C++ // [[Programmierung]]</sub>
____
## How to:
```cpp
int a;
int b = 7;
double c;

//zuweisungen
c = 17.5;
a = b + 3 // => a = 10
```

## Aufgabe 1.1
```cpp
float x;
x = 7 / 8; // => x = 0, da datentyp integer ist
```

```cpp
int var1 = 27, var2 = 33;
var1 = var1 + var2 // = 60

var2 = var2 / 2 // = 16,5 = 16

var2 = var2 / var1 // = 16 / 60 = 0
```

## Aufgabe 1.2
```cpp
char buchstabe1;

buchstabe1 = 'A';

buchstabe1++; // 66 = B;

buchstabe1 += 3; // 66+3 = E;
```
## Aufgabe 1.3
```cpp
double komma1 = 2.5;
float komma2 = 1.9;
int ganzzahl1 = 7;
long ganzzahl2 = 8;
char buchstabe2 = 'D';

komma1 = (ganzzahl1 / ganzzahl2) + 3; // (7 / 8) + 3 = 0 + 3 = 3

komma2 = ganzzahl2; // = 7

ganzzahl1 = buchstabe2; // = 68
```
## Aufgabe 2
```cpp
#include <iostream>  
#include <stack>  
using namespace std;  
  
int main() {  
    stack<int> s;  
    int summe = 0;  
  
    for(int i = 1; i < 4; i++) {  
        cout << "i" << i << endl;  
        s.push(i);  
    }  
    while(!s.empty()) {  
        summe += s.top();  
        s.pop();  
    }  
    cout << "Summe: " << summe << endl;  
    return 0;  
}
```