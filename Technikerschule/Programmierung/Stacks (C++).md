<sub class="descriptionSection">18-09-2024 04:20:pm // #C++ // [[Programmierung]]</sub>
____
Stacks sind Datenstrukturen in C++, die mehrere Werte hinterinander speichern können

## Stack Operations
Die Stack class hat die folgenden functions:
```cpp
#include <stack>
#include <iostream>
using namespace std

int main(){
	//initialized einen Stack in dem Double gespeichert werden können
	auto stackTest = stack<double>();

	//liest den obersten wert im Stack:
	cout << stackTest.top() << endl;

	//removed den obersten wert im Stack:

	stackTest.pop();

	//gibt die länge des stapels aus
	cout << stackTest.size();

	//fügt einen wert zum stack hinzu
	stackTest.push(1.5);

	return 0;
}
```

## Usecases
? Good question. Eigentlich wäre in jeder Situation die mir einfällt ein Array besser. Prob. ist ein Stack schneller als ein Array.