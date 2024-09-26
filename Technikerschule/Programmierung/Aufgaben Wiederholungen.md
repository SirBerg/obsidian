<sub class="descriptionSection">25-09-2024 05:14:pm // #Übung // [[Programmierung]]</sub>
____
## Aufgabe 2.1
```cpp
#include <iostream>  
  
using namespace std;  
int main() {  
    for(int i = 1; i <=19; i = i+2) {  
        cout << i << endl;  
    }  
    return 0;  
}
```
## Aufgabe 2.2
```cpp
#include <iostream>  
  
using namespace std;  
int main() {  
    int top = 20;  
    for(int i = 1; i <= 6; i++) {  
        cout << top << " " << i << " ";  
        top = top - 2;  
    }  
  
    return 0;  
}
```
## Aufgabe 3
![[Pasted image 20240925142607.png]]
## Aufgabe 3.2
```text
i = 0
j = 0 j = 1 .. j = 9
i = 1
j = 0 j = 1 .. j = 9
..
i = 9
j = 0 j = 1 .. j = 9
```
## Aufgabe 3.4
```cpp
#include <iomanip>  
#include <iostream>  
  
using namespace std;  
int main() {  
    int i,j;  
    for (i = 0; i < 10; i++)  
    {  
        cout << setw(2) << setfill('0') << i << ". ";  
        for (j=i;j < 10+i; j++)  
        {  
            cout << setw(2) << setfill('0') << j << " ";  
        }  
        cout << endl;  
    }  
  
    return 0;  
}
```
## Aufgabe 4
```cpp
#include <iomanip>  
#include <iostream>  
  
using namespace std;  
int main() {  
    char ch = 'A';  
    char ch2 = 'A';  
    char ch3 = 'A';  
    int i = 0;  
    while(ch <= 'Z') {  
        while (ch2 <= 'Z') {  
            while(ch3 <= 'Z') {  
                cout << i<< ". "<< ch << ch2 << ch3 << endl;  
                ch3++;  
                i++;  
            }  
            ch3 = 'A';  
            ch2++;  
        }  
        ch2 = 'A';  
        ch++;  
    }  
  
    return 0;  
}
```
## Expertenaufgabe
```cpp
#include <iomanip>  
#include <iostream>  
  
using namespace std;  
int main() {  
    int marginleft = (80 - 21) / 2;  
    int i = 1;  
    cout << setw(marginleft);  
    while(i <= 49) {  
        if((i - 1) % 7 == 0) {  
            cout << setw(marginleft + 2) << i << " ";  
        }  
        else {  
            cout << setw(2) << i << " ";  
        }  
        if((i % 7) == 0) {  
            cout << endl;  
            cout << setw(marginleft);  
        }  
        i++;  
    }  
    return 0;  
}
```
## Expertenaufgabe 2
```cpp
#include <iostream>  
  
using namespace std;  
int main() {  
    int i = 1;  
    int lastInt = 0;  
    while (i > lastInt) {  
        lastInt = i;  
        i++;  
    }  
    cout << lastInt << endl;  
    return 0;  
}
```