<sub class="descriptionSection">25-09-2024 05:15:pm // #Wiki // [[Programmierung]]</sub>
____
In C++ gibt es ein paar Bitwise Operatoren die in bestimmten Situationen sehr hilfreich sein können.

## Was sind Bitwise Operations?
Bitwise operations ermöglichen die Manipulation von einzelnen Bits in Variablen. Als Beispiel könnte man 2 quadrieren in dem man:
```cpp
int n = 2
n << 1 //verschiebt alle bits in der variable n um 1 nach links
```
Bitwise Operations sind sehr effizient und können gut genutzt werden in prozessor limited oder embeded environments .
## Welche Bitwise Operations gibt es?
Es gibt die folgenden Bitwise operatoren:
```cpp
x << y // die variable x wird um y bits nach links verschoben (quadriert, potenziert)
x >> y // die variable x wird um y bits nach rechts verschoben (wurzel ziehen)

x & y // bitwise AND

x | y // bitwise OR

x ^ y // btiwise XOR

~ x // einerkomplement von x

```
## Vorteile von Bitwise Operations
Bitwise operations lassen den Programmierer direkt die Bits verändern und elimieren sehr viel OS overhead. Somit sind Bitwise Operations sehr effizient und können gut in embeded environments benutzt werden.