<sub class="descriptionSection">20-09-2024 10:46:am // #Mathe // [[Mathematik]]</sub>
____
Diese Seite behandelt #Binome in der [[Mathematik]]. Dieser Artikel ist Teil des Mathematik [[Mathematik Grundwissen|Grundwissens]]
## Was sind [Binome](https://de.wikipedia.org/wiki/Binom)?
Binome sind Terme mit einer potenzierten Klammer in der zwei Werte stehen. Sie sind vor allem nützlich wenn man Terme ausklammern möchte:
```text
3a²x² - 12a² + 12a² = 
	3a² (x² - 2x * 2 + 2²) =
	3a² (x - 2)
```
Es gibt drei verschiedene Binomische formeln:
### Die drei Binomischen Formeln

#### Erste binomische Formel:

> (a+b)² = a² + 2ab + b²

Hier zu beachten ist vor allem der zweite Term. Im zweiten Term sehen wir, dass es nur + Zeichen geben kann, wenn wir zur ersten Klammer umformen wollen.

#### Zweite binomische Formel:

> (a - b)² = a² - 2ab + b²

Wie in der ersten binomischen Formel, ist wieder der zweite Term extrem wichtig. In ihm können wir sehen das, statt nur + Zeichen, nun ein - Zeichen vorhanden ist. Hierdurch **muss** in der potenzierten klammer ein minus stehen, sonst kann der Term nicht mehr korrekt ausgeklammert werden.

#### Dritte binomische Formel:

> (a+b)(a-b) = a² - b²

Im gegensatz zu den ersten zwei Formeln, ist diese mehr ein recheninstrument. Sehr nützlich beim kürzen und vereinfachen von termen.

## Lösungsansätze und Beispiele

> [!NOTE] Lösungshilfe
> Mir hat beim Lösen von Binomen geholfen, aus der kleinsten Zahl die Wurzel zu ziehen und dann zu sehen ob man bei den anderen Zahlen im Term auch diese Zahl ausklammern könnte

```
15x² + 30xy + 15y² = 15(x + y)² <- 1ste Binomische Formel

18x³ - 60x²a + 50xa² = <- Hier konnte nur die zwei Ausgeklammert werden
	2x (9x² - 30xa + 25a²) = <- Zweite Binomische Formel angewendet
	2x (3x - 5a)²

4x⁵ - 25x⁴ + 36x³ = <- 4x³ ist das höchste was Ausgeklammert werden konnte 
	4x³ (x² - 6x + 9) = <- Zweite Binomische Formel anwenden
	4x³ (x - 3)²
```

## Rechenweg wenn eine Nummer fehlt / ein Rechenzeichen fehlt
Wenn es eine fehlende Nummer gibt dann kann diese ausgerechnet werden in einer Binomischen Formel, da es immer eine Zahl gibt die aus den anderen beiden bestehen muss. Die mittlere Zahl hier, kann als "Checksum" betrachtet werden:
$$
0,16b^2 - 4,8bc - 36c^2 = (0,4b - 6c)^2
$$
Die "Checksum" entsteht dadurch, dass die Klammer für die Binomische formel ja Ausmultipliziert werden muss. Wenn also eine Aufgabe wie diese hier gegeben ist:
$$
\frac{1}{16}r^4 + [leer] + 2 = ([leer] + [leer])^2
$$
Kann man die restlichen Zeichen so ausrechnen:
Die Klammer setzt sich so zusammen:
$$
(\sqrt\frac{1}{16} + \sqrt2)^2
$$

> [!NOTE] Erklärung
> Die Wurzel muss aus den beiden ausmulitplizierten Zahlen gezogen werden, da sonst wenn man die Klammer ausmultiplizieren würde, nicht $\frac{1}{16}$ und 2 rauskommen würden

Die aktuelle Rechnung (mit ausgerechneten Wurzeln) sieht also so aus:
$$
\frac{1}{16}r^4 + [leer] + 2 = (\frac{1}{4}r^2 + \sqrt{2})^2 <- \text{Wurzel aus zwei kann nicht gerechnet werden}
$$
Die einzige leere stelle kann dann ausgerechnet werden indem man einfach für die binomische formel:
$$
a*b*2
$$

rechnet
In dem konkreten beispiel:
$$
\frac{1}{4}r^2*\sqrt{2}*2 = \frac{\sqrt2}{2}r^2
$$

Somit sieht die Aufgabe am ende so aus:
$$
\frac{1}{16}r^4 + \frac{\sqrt2}{2} + 2 = (\frac{1}{4}r^2 + \sqrt2)^2 
$$

## Wenn eine linke oder rechte Zahl fehlt

Gegeben ist die Aufgabe:
$$
1,21a^2 - \frac{1}{5}ab + [leer] = (1,1a \text{ [leeresRechenZeichen] } [leer])^2
$$
Da wir schon sehen können anhand des Minus im linken Term das das die zweite Binomische Formel sein muss, können wir davon ausgehen das das leere Rechenzeichen ein - sein *muss*.
Dadurch sieht die Aufgabe so aus: 
$$
1,21a^2 - \frac{1}{5}ab + [leer] = (1,1a - [leer])^2
$$
Jetzt können wir den Rechten Teil in der Klammer auflösen. Da die wir die "Checksum" von $\frac{1}{5}ab$ haben, können wir den Rechten teil mit Hilfe der Formel von oben berechnen:
$$
a*b*2 = c => b = \frac{c}{a*2}
$$
$$
1,1a *[leer]*2 = \frac{1}{5}ab => [leer] = \frac{\frac{1}{5}ab}{1,1a*2} = \frac{1}{11}b
$$
Somit ist die Lösung:
$$
1,21a^2 - \frac{1}{5}ab + \frac{1}{121}b^2 = (1,1a - \frac{1}{11}b)^2
$$