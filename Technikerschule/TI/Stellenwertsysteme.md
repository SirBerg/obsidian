<sub class="descriptionSection">26-09-2024 11:56:am // #Systeme // [[TI]]</sub>
____
## Allgemeine Schema für Stellenwertsysteme

##### Für eine beliebige Basis `b`

$$
Z_{10}=\sum_{i=0}^{n-1}*a_i *b
$$
In der Formel bezieht sich:
- `b` auf die Basis, also im Binärsystem 2
- `a` auf die Stellenziffer 

> [!NOTE] Merksatz
> Um die Zahlen eindeutig darstellen zu können, werden `b` verschiedene Ziffern benötigt:
> $$
> 0 \leq a_i < b
> $$
> **Merke: Aus einer Ziffer wird erst dann eine Zahl, wenn die Ziffer mit dem Stellenwert multipliziert wird.**

##### In der IT
Die Kleinste Informationseinheit ist 1 Bit.

=> Ein Bit kann 2 Zustände annehmen -> 2 Verschiedene Ziffern, diese Ziffern sind 0 & 1

=> Dualzahlen mit der _Basis_ b = 2 
So können diese Zahlen bestimmt werden, mithilfe der Formel von [[#Für eine beliebige Basis `b`|oben]]:
$$
0 \leq a_i < 2
$$
Die Stellenwerte sind ganzzahlige Potenzen zur Basis b = 2

| $Z_{(2)} =$ | 0     | 1     | 1     | 0     | 1     | 1     | 1     | 0     | Ziffernfolge           |
| ----------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ---------------------- |
|             | $a_7$ | $a_6$ | $a_5$ | $a_4$ | $a_3$ | $a_2$ | $a_1$ | $a_0$ | **Variablen**          |
|             | 7     | 6     | 5     | 4     | 3     | 2     | 1     | 0     | **Stellen**            |
|             | $2^7$ | $2^6$ | $2^5$ | $2^4$ | $2^3$ | $2^2$ | $2^1$ | $2^0$ | **Stellenwerte**       |
|             | 128   | 64    | 32    | 16    | 8     | 4     | 2     | 1     | **Tatsächlicher Wert** |
Es wird der Stellenwert \* die Ziffernfolge genommen und addiert um das Dezimal Ergebnis zu bekommen
$$
Z_{(10)} = 0*2^0 + 1*2^1 + 1*2^2 + 1*2^3 + 0*2^4 + 1*2^5 + 1*2^6 + 0*2^7
$$
$$
= 0 * 1 + 1*2 + 1*4 + 1*8 + 0*16 + 1*32 + 1*64 + 0*128
$$
$$
= 2 + 4 + 8 + 32 + 64
$$
$$
= 110_{(10)}
$$
##### Übung: 
Ein Kakadu hat 4 Zehen pro Kralle
=> 8 Zehen insgesamt. Er zählt seinen Körnervorrat! 

$$
Z_{(8)} = 274
$$
Wieviele Körner sind dies im Dezimalsystem?

| $Z_{(8)}=$ | 2     | 7     | 4     | Ziffernfolge       |
| ---------- | ----- | ----- | ----- | ------------------ |
|            | $a_2$ | $a_1$ | $a_0$ | Variablen          |
|            | 2     | 1     | 0     | Stellen            |
|            | $8^2$ | $8^1$ | $8^0$ | Stellenwerte       |
|            | 64    | 8     | 1     | Tatsächlicher Wert |
$$
Z_{(10)} = 4*1 + 7*8 + 2*64 = 188_{(10)}
$$
##### Umrechnung von Dezimalzahlen größer 1 (Ganzzahl) in ein beliebiges Zahlensystem
