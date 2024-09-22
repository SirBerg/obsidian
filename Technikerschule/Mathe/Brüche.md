<sub class="descriptionSection">22-09-2024 11:55:am // #Grundwissen // [[Mathematik]]</sub>
____
## Terminologie
### Zähler / Nenner
Bei einem Bruch nennt man die obere Zahl den "Zähler", die untere Zahl den "Nenner":
$$
\frac{\text{Zähler}}{\text{Nenner}}
$$
### Erweitern / Kürzen
Erweitern und Kürzen sind rechenoperationen mit einem Bruch. Sie sind nützlich wenn man brüche addieren und subtrahieren möchte, für division und multiplikation sind sie nicht so nützlich.
Erweitern muss man immer bei Zähler und Nenner **mit der selben Zahl / dem selben Wert**, damit der endgültige Wert des Bruches nicht verändert wird, genauso mit dem kürzen aber in die andere Richtung. Beim Kürzen werden gleiche Terme aus dem Bruch gestrichen, dabei müssen diese im Zähler und Nenner existieren und es müssen Multiplikationen und Divisionen sein. Addition und Subtraktion **dürfen nicht gekürzt werden**


> [!NOTE] Note
> Beim Erweitern und Kürzen hilft es oft, die Zahlen in ihre Primfaktoren zu zerlegen.


#### Beispiel fürs erweitern:
$$
\text{Erweitern mit (x+4): } \frac{(3x+6)*(x+4)}{(x^2-4)*(x+4)}
$$

$$
\frac{x}{6} + \frac{1}{15}
$$
Erweiter den ersten bruch mit 5, den zweiten mit 2 um auf den selben Nenner zu kommen:
$$
\frac{5x}{30} + \frac{2}{30} = \frac{5x+2}{30}
$$
#### Anderes Beispiel:
Aufgabenstellung:
$$
\frac{2x+1}{3x+21} - \frac{x^2}{2x^2-98}
$$
Ausklammern:
$$
\frac{2x+1}{3(x+7)} - \frac{x^2}{2(x^2 - 49)}
$$
Der Nenner im zweiten Bruch ist eine Binomische Formel, deswegen kann man den Bruch auch so schreiben:
$$
\frac{2x+1}{3(x+7)} - \frac{x^2}{2(x + 7)(x-7)}
$$
Jetzt können wir die beiden Nenner ausgleichen, in dem wir die jeweils fehlenden Teile in den anderen Nenner schreiben. In diesem Fall fehlt im Linken bruch $2(x-7)$ und im rechten $3$ :

> [!Warning] Achtung
> Beim erweitern müssen die selben Rechenoperationen die im Nenner passieren auch im Zähler passieren!

$$
\frac{(2x+1)* 2(x-7)}{3(x+7) * 2(x-7)} - \frac{3*x^2}{3*2(x + 7)(x-7)}
$$
Da jetzt die Nenner gleich sind, können wir die brüche so schreiben:
$$
\frac{((2x+1)* 2(x-7)) - 3x^2}{3(x+7) * 2(x-7)}
$$
Das einzige was jetzt noch funktioniert ist ausrechnen:
Multiplizere innheralb der Klammern:
$$
\frac{(2x+1)*(2x-14) - 3x^2}{6*(x+7)(x-7)}
$$
Klammern ausmultiplizieren:
$$
\frac{4^2 - 28x + 2x - 14 - 3x^2}{6(x-7)^2}
$$
Fertig zusammenrechnen und vereinfachen:
$$
\frac{x^2 - 16x - 14}{6(x-7)^2}
$$
#### Beispiel fürs Kürzen:
Aufgabenstellung:
$$
\frac{6x-15}{24x+32}*{\frac{9x+12}{10x-25}}
$$
Zuerst alles ausklammern was geht:
$$
\frac{3(2x-5)}{8(3x + 4)}*{\frac{3(3x+4)}{5(2x-5)}}
$$
Jetzt kann man kürzen:
$$
\frac{3\cancel{(2x-5)}}{8\cancel{(3x + 4)}}*{\frac{3\cancel{(3x+4)}}{5\cancel{(2x-5)}}}
$$
Jetzt sehen die Brüche so aus:
$$
\frac{3}{8}*\frac{3}{5} = \frac{9}{40}
$$
## Addition und Subtraktion
Das wichtigste bei Addition und Subtraktion ist das **bei Brüchen beide Nenner gleich sein müssen**. Das kann durch Kürzen und Erweitern erreicht werden, wie oben beschrieben.
### Beispiel:
$$
\frac{1}{2}+\frac{32}{12}
$$
Am einfachsten können wir einen gemeinsamen Nenner ermitteln, in dem wir sehen wie oft der kleinste Nenner in den größeren passt (großer nenner, durch kleinen):
$$
12/2 = 6
$$
Jetzt erweitern / kürzen wir:
$$
\frac{1*3}{2*3} + \frac{32/2}{12/2}
$$
=
$$
\frac{3}{6}+\frac{16}{6}
$$
Jetzt können wir zusammenrechnen:
$$
\frac{3+16}{6} = \frac{19}{6}
$$
Da wir ergebnisse immer so weit wie möglich gekürzt angeben müssen, müssen wir schauen das wir nicht mehr weiter den bruch verkleinern können. In diesem fall **kann man nicht mehr weiter verkürzen**.
## Multiplikation
Multiplikation ist sehr einfach bei Brüchen, da man einfach nur Zähler und Nenner mit dem jeweils anderen multiplizieren muss.
### Beispiel:
Aufgabenstellung:
$$
\frac{x^2-a^2}{15x}*\frac{x^2}{x+a}
$$
Dritte Binomische Formel anwenden:
$$
\frac{(x-a)(x+a)}{15x}*\frac{x^2}{x+a}
$$
Da wir hier Multiplizieren, dürfen wir einfach so kürzen:
$$
\frac{(x-a)\cancel{(x+a)}}{15x}*\frac{x^2}{\cancel{x+a}}
$$
Der Term sieht jetzt so aus:
$$
\frac{(x-a)}{15x}*\frac{x^2}{1}
$$
Jetzt können wir zusammen rechnen:
$$
\frac{(x-a)*x^2}{15x*1}
$$
Jetzt kann man den Term oben auch so schreiben:
$$
\frac{(x-a)*x*x}{15x}
$$
Somit lässt sich ein x kürzen:
$$
\frac{(x-a)*x*\cancel{x}}{15\cancel{x}}
$$
Das ergbniss (nachdem die Klammer ausmultipliziert wurde) ist also:
$$
\frac{x^2*ax}{15}
$$
## Division
Die Division funktioniert fast so wie die Multiplikation, nur das der Bruch durch den geteilt wird, als Keersumme dargestellt wird (er wird also umgedreht und mit dem umgedrehten Bruch multipliziert).
### Beispiel:
Angabe:
$$
\frac{\frac{1}{b-a}}{\frac{1}{a^2-b^2}}
$$
Da ein Bruch auch einfach nur eine Division darstellt, kann diese Aufgabe auch so geschrieben werden:
$$
\frac{1}{b-a}:\frac{1}{a^2-b^2}
$$
Jetzt können wir die den zweiten Bruch umdrehen und statt : das * Zeichen schreiben:
$$
\frac{1}{b-a}*\frac{a^2-b^2}{1}
$$
Beim rechten bruch gibt es eine 3. Binomische Formel, wenn wir die ausschreiben:
$$
\frac{1}{b-a}*\frac{(a-b)*(a+b)}{1}
$$

> [!Warning] Achtung
> Wenn man das jetzt hier sieht, sieht man vielleicht das man (a-b) mit (b-a) kürzen könnte. **Das ist nicht erlaubt, da es nicht die selben Zahlen sind**. Um zu kürzen müssen wir aus den oberen rechten klammern eine -1 ausklammern.

> [!NOTE] -1 Ausklammern
> -1 kann man ausklammern um die Vorzeichen umzudrehen

$$
\frac{1}{b-a}*\frac{(a + b)*-1 (-a - b)}{1}
$$

Jetzt kann man b-a kürzen mit oben rechts:
$$
\frac{1}{\cancel{b-a}}*\frac{-1* \cancel{(-a + b)}*(a + b)}{1}
$$
Jetzt sieht es so aus:
$$
\frac{1}{1}*\frac{-1*(a + b)}{1}
$$
$\frac{1}{1}$ kann man auslassen da es * 1 bedeutet. Jetzt können wir wieder die -1 auch in die Klammer reinschreiben, und die lösung sieht am ende so aus:
$$
\frac{1}{1}*\frac{-1*(a + b)}{1} = \frac{-1 (a+b)}{1} = -1 * (a+b) = - b - a
$$