<sub class="descriptionSection">23-09-2024 09:26:am // #Datenbanken  // [[Databases]]</sub>
____
Ansi-Sparc Architektur (auch Drei-Schema-Architektur, Drei-Ebenen-Architektur, etc. genannt) beschreibt die grundlegende Trennung verschiedener Beschreibungsebenen für Datenbankschemas.
## Die drei Ebenen der Ansi-Sparc Architektur
Die Ansi-Sparc Architektur hält verschiedene features und teile eines DBMS auseinander in die folgenden Ebenen:
- Die externe Ebene stellt Benutzern und Anwendungen individuelle Access möglichkeiten bereit.
- Die konzeptionelle Ebene beschreibt welche Daten in der Datenbank gespeichert sind, sowie deren Beziehungen zueinander. Das erklärte Ziel hier ist generell das es keine [[Dateninkonsistenz und Anomalien#Redundanz|Redundanzen]] in den Daten gibt. Hier findet die Daten [[Dateninkonsistenz und Anomalien#Normalisierung|Normalisierung]] statt.
- Die interne Ebene lässt das DBMS physisch die Daten abspeichern. Es ist die schicht die am ende die Daten von der Platte holt und auch wieder dort ablegt
## Vorteile der Architektur
Da die Ebenen getrennt sind, ist es einfacher für das DBMS tatsächlich die Daten zu speichern und abzurufen. 
- Physiche änderungen im Speichermedium ändern nichts in der konzeptionellen und externen Ebene
- Die konzeptionelle Ebene ist getrennt, somit können Applications geändert werden ohne das die änderungen andere Applications affecten.
Allgemein ist die Architektur sehr viel Robuster gegenüber Änderungen als andere Methoden.