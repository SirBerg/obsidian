<sub class="descriptionSection">24-09-2024 05:34:pm // #Datenbanken // [[Databases]]</sub>
____
Wenn mit Daten gearbeitet wird, können 3 Arten von Anomalien auftreten. Quasi alle diese Anomalien können eliminiert werden wenn eine Datenstruktur normalisiert wird.
## Anomalie No.1: Änderungs-Anomalie
Wenn dieselben Daten an unterschiedlichen Stellen gespeichert werden, müssen die Daten überall geändert werden. Sonst entsteht inkonsistenz.
![[image_1727154980521_0.png]]
Hier wurde die Telefonnummer von Hans Schmitz im vorherigem Datensatz übersehen und nicht geändert.
## Anomalie No.2: Einfüg-Anomalie
Tritt auf, wenn Daten eingegeben werden **müssen** aber nicht bekannt sind (im Bild rot).
![[image_1727155158296_0.png]]
## Anomalie No. 3: Lösch Anomalie
Eine Lösch Anomalie tritt auf wenn man alle Daten eines [[DBMS Begriffe#Datensatz|Datensatz]] löscht, aber dadurch auch andere daten gelöscht werden, was aber nicht gewollt war (i.e ungewollter Datenverlust).
![[image_1727155353428_0.png]]
Wenn in diesem Bild [[DBMS Begriffe#Datensatz|Datensatz]] 8 und 9 gelöscht werden gehen auch die informationen zum Berater verloren.
## Redundanz
Von Datenredundanz wird gesprochen wenn Daten mehrfach abgespeichert werden. Es ist erstrebenswert das so gut wie möglich zu vermeiden und meistens ist das auch relativ einfach, allerdings muss auch auf einen Performance und Usability aspekt geachtet werden. Redundanzen werden meist in der DB Plannungsphase direkt per Normalisierung ausgearbeitet.
### Normalisierung
Mit Normalisierung werden Datenredundanzen eliminiert. Ein Beispiel:

Angenommen wir haben die Tabellen "Users" und "Products":
![[Pasted image 20240924171435.png]]
Wenn wir jetzt eine Tabelle "Payments" einführen wollen und **nicht normalisieren würden**. Müsste die Tabelle so aussehen:
![[Pasted image 20240924171612.png]]
Das ist nicht sehr effizient, da der Produktname, der Username etc. öfter abgespeichert werden muss.
Wenn man normalisieren würde könnte die Tabelle so aussehen:
![[Pasted image 20240924171818.png]]Hier wird ein Produkt und User nur einmal gespeichert. In der Payment Tabelle stehen jetzt nur **referenzen** zu den anderen Records. Die Tabelle ist somit Normalisiert, da keine Datenredundanzen mehr entstehen.