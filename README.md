# Übung 4 - Verzweigungen

Erstellen Sie sich für die Theorieaufgaben ein eigenes File und laden Sie dieses auch in Ihr Repository. 

**Achtung:** Die beiliegende Main-Klasse beinhaltet die Testfälle für die Aufgaben 1, 2 und 3. 
Wenn Sie vorerst nur eine der drei Aufgaben testen wollen, kommentieren Sie die Testfälle 
der anderen Aufgaben in der Main-Klasse aus.

## 1. Aufgabe

Folgendes Klassendiagramm soll umgesetzt werden:

<p align="center">
  <img src="/assets/images/UML1.png" alt="UML Aufgabe 1" />
</p>

**Spezifikationen:**
- Im Konstruktor müssen statt der Zuweisung die `set`-Methoden aufgerufen werden.
- Die Parameternamen des Konstruktors müssen gleich den Eigenschaftsnamen sein. 
- `print()`: Gibt alle Eigenschaften in der Konsole aus. Folgendermaßen soll die Ausgabe aussehen:  
##############################  
\## Aufbohren: true  
\## Besitzer: Max Muster  
\## Kubikzentimeter: 80  
\## Kilometerstand: 150  
\## Höchstgeschwindigkeit: 40  
\##############################

- `fahren(double m)`: Das Moped wird um m (in Metern) gefahren. Dadurch ändert sich natürlich der `kmStand`. Es sollen nur Werte von 1 bis 1000 zugelassen werden. Bei einem ungültigen Wert soll 0 zurückgeben und eine Fehlermeldung ausgegeben werden. 
- `service()`: Das Moped muss zum Service. Der Rückgabewert sind die Kosten, die sich aus dem `kmStand * 2€` berechnen. Sollte das Moped aufgebohrt sein, so zahlt man zusätzlich 100€. Nach dem Service soll das Moped nicht mehr aufgebohrt sein.
- `aufbohren()`: Das Moped wird aufgebohrt, wodurch sich seine ccm und die Maximalgeschwindigkeit verdoppeln.

## 2. Aufgabe

Folgendes Klassendiagramm soll umgesetzt werden:

<p align="center">
  <img src="/assets/images/UML2.png" alt="UML Aufgabe 2" />
</p>

**Spezifikationen:**
- Der Standardkonstruktor erzeugt ein Auto-Objekt mit sinnvoll gewählten Default-Werten.
- Wird einer `set`-Methode ein unerlaubter Wert übergeben, soll eine Fehlermeldung ausgegeben und ein sinnvoller Default-Wert gesetzt werden.
- `baujahr` muss größer 1950 sein und darf nur einmal einen Wert erhalten. Wie kann man eine `set`-Methode so realisieren, dass sie nur beim erstmaligen Aufruf einen Wert übernimmt?
- Ein Elektrofahrzeug besitzt kein Schaltgetriebe und ist daher immer ein Fahrzeug mit Automatik. Worauf ist zu achten wenn `setElektrisch()` oder `setAutomatik()` aufgerufen wird?
- `sitzplaetze` erhält immer einen Wert von 2 bis 9.
- `kilometerstand` ist stets ein positiver Wert größer-gleich 0 und darf nur erhöht werden.
- `berechneAlter()` soll das Alter des Autos im Jahr 2025 berechnen. Welche Werte dürfen Sie zulassen?
- `berechneAlter(jahr: int)` soll das Alter des Autos im Jahr `jahr` brechnen. Welche Werte dürfen Sie zulassen?
- `printInfo()` soll alle Eigenschaften schön formatiert in der Konsole ausgeben.
- `fahren()` erhöht kilometerstand um 10 km. 
- `fahren(strecke: int)` erhöht kilometerstand um den Wert `strecke` (in km). Bei einem ungültigen Wert soll eine Fehlermeldung auf der Konsole ausgegeben werden.

## 3. Aufgabe

Folgendes Klassendiagramm soll umgesetzt werden:

<p align="center">
  <img src="/assets/images/UML3.png" alt="UML Aufgabe 3" />
</p>

Um den `preis`zu setzen, muss folgendes gelten:

<table align="center">
<tr><td>

| <code>preis</code>  | <code>farbe</code>  | <code>dach</code>  |
|:---:|:---:|:---:|
| <code>>= 200</code>  | <code>true</code>  | <code>beliebig</code>  |
| <code>>= 100</code>  | <code>false</code>  | <code>true</code>  |
| <code>40 - 99</code>  | <code>false</code>  | <code>false</code>  |

</td></tr> </table>

**Achtung:**
- Werden die Bedingungen nicht erfüllt, soll eine Fehlermeldung ausgegeben werden und der Preis soll den kleinsten erlaubten Wert annehmen.
- `setFarbe()` und `setDach()` dürfen keine inkonsistenten Objektzustände erzeugen.
- `print()` soll alle Eigenschaften schön formatiert in der Konsole ausgeben.

Beispielhafte Aufrufe von `setPreis(preis)`:

<table align="center">
<tr><td>

| <code>preis</code>  | <code>farbe</code>  | <code>dach</code>  | Objekt erzeugt mit <code>preis</code>  | Terminalfenster  |
|:---:|:---:|:---:|:---:|:---:|
| <code>100</code>  | <code>true</code>  | <code>true</code>  | <code>200</code>  | <code>Fehler: Preis mit Farbe ist zu klein.</code>  |
| <code>90</code>  | <code>false</code>  | <code>true</code>  | <code>100</code>  | <code>Fehler: Preis mit Dach ist zu klein.</code>  |
| <code>39</code>  | <code>false</code>  | <code>false</code>  | <code>40</code>  | <code>Fehler: Preis ohne Dach und Farbe ist zu klein.</code>  |
| <code>233</code>  | <code>false</code>  | <code>false</code>  | <code>40</code>  | <code>Fehler: Preis ohne Dach und Farbe ist zu groß.</code>  |
| <code>233</code>  | <code>false</code>  | <code>true</code>  | <code>233</code>  |   |
</td></tr> </table>

**Probieren Sie die folgende Aufgabe ohne Hilfe der IDE oder des Internets.**

## 4. Aufgabe

Welche Ausgabe liefert folgender Codeausschnitt?

<p align="center">
  <img src="/assets/images/Cod1.png" alt="Codeausschnitt" />
</p>
