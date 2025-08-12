---
title: Java
created: '2025-08-07T09:11:57.638Z'
modified: '2025-08-12T08:38:33.434Z'
---

# Java 

Java ist eine objektorientierte Programmiersprache, die weltweit sehr verbreitet ist.  
Sie ist bekannt für ihre Plattformunabhängigkeit, weil Java-Programme nicht direkt als Maschinencode ausgeführt werden,  
sondern zuerst in **Bytecode** kompiliert werden. Dieser Bytecode läuft dann auf der **Java Virtual Machine (JVM)**,  
die es für fast jedes Betriebssystem gibt.  

Das macht Java besonders geeignet für Anwendungen, die auf verschiedenen Geräten und Systemen laufen sollen –  
von Desktop-Programmen über Web-Anwendungen bis hin zu Apps für Android.

---
## Wichtige Commands
- `import java.util.Scanner;`: Importiert die Scanner-Klasse, um Eingaben von der Konsole zu lesen  
- `public class Klassenname { ... }`: Definiert eine öffentliche Klasse  
- `public static void main(String[] args) { ... }`: Startpunkt des Programms  
- `Scanner scanner = new Scanner(System.in);`: Erstellt einen Scanner zum Einlesen von Eingaben  
- `System.out.print("Text");`: Gibt Text ohne Zeilenumbruch aus  
- `System.out.println("Text");`: Gibt Text mit Zeilenumbruch auf der Konsole aus  
- `int variable = scanner.nextInt();`: Liest eine ganze Zahl von der Konsole ein und speichert sie in einer int-Variable  
- `if (Bedingung) { ... }`: Führt Code aus, wenn die Bedingung wahr ist  
- `else { ... }`: Führt Code aus, wenn die Bedingung nicht wahr ist  
- `else if (Bedingung) { ... }`: Prüft eine weitere Bedingung, wenn die vorherige nicht zutrifft  
- `%`: Modulo-Operator – gibt den Rest einer Division zurück  
- `>=`: Vergleichsoperator „größer gleich“  
- `==`: Vergleichsoperator „gleich“  
- `!=`: Vergleichsoperator „ungleich“  
- `package paketname;`: Legt das Paket fest, zu dem die Datei gehört  
- `System.out.printf("Format", werte);`: Gibt formatierten Text aus  
- `Datentyp variable = Wert;`: Deklariert und initialisiert eine Variable (z. B. `String name = "Max";`)  
- `final Datentyp NAME = Wert;`: Deklariert eine Konstante  
- `switch (Variable) { case ...: break; ... }`: Mehrfachauswahl abhängig vom Wert einer Variablen  
- `while (Bedingung) { ... }`: Wiederholt Code, solange die Bedingung wahr ist  
- `do { ... } while (Bedingung);`: Führt Code mindestens einmal aus, prüft dann die Bedingung  
- `for (Start; Bedingung; Schritt) { ... }`: Schleife mit fester Anzahl von Durchläufen  
- `break;`: Beendet Schleife oder Switch-Block  
- `continue;`: Überspringt den Rest einer Schleifeniteration  
- `return Wert;`: Gibt einen Wert aus einer Methode zurück und beendet sie  
- `scanner.nextLine();`: Liest eine komplette Textzeile von der Konsole ein  
- `scanner.nextDouble();`: Liest eine Gleitkommazahl von der Konsole ein  
- `variable.equals("Text")`: Vergleicht den Inhalt zweier Strings  
- `// Kommentar`: Einzeiliger Kommentar  
- `/* Kommentar */`: Mehrzeiliger Kommentar  


---
## Wichtige Datentypen

- `byte`: 8-Bit ganze Zahl (-128 bis 127) – sehr kleiner Zahlenbereich, spart Speicherplatz  
- `short`: 16-Bit ganze Zahl (-32'768 bis 32'767) – etwas größerer Zahlenbereich  
- `int`: 32-Bit ganze Zahl (-2'147'483'648 bis 2'147'483'647) – Standard für Ganzzahlen  
- `long`: 64-Bit ganze Zahl (-9'223'372'036'854'775'808 bis 9'223'372'036'854'775'807) – sehr große Ganzzahlen  
- `float`: 32-Bit Gleitkommazahl – Dezimalzahlen mit ca. 7 Stellen Genauigkeit  
- `double`: 64-Bit Gleitkommazahl – Dezimalzahlen mit ca. 15 Stellen Genauigkeit  
- `char`: 16-Bit Unicode-Zeichen – einzelne Buchstaben oder Symbole  
- `boolean`: Wahrheitswert (`true` oder `false`) – nur zwei mögliche Zustände  
- `String`: Zeichenkette (kein primitiver Datentyp) – Text in Anführungszeichen  

---



## Aufbau eines Java-Programms

1. **Dateiname = Klassenname**  
   - Wenn die Klasse `Main` heißt, muss die Datei `Main.java` heißen.  
2. **`public class`**  
   - Jede Java-Datei hat mindestens eine Klasse, in der der Code steht.  
3. **`main`-Methode**  
   - Diese Methode ist der **Startpunkt** jedes Java-Programms:  
     ```java
     public static void main(String[] args) { ... }
     ```
4. **Code-Blöcke** werden mit geschweiften Klammern `{}` markiert.  
5. **Jede Anweisung** endet mit einem Semikolon `;`.  
6. **Ausgabe auf der Konsole**:  
   - `System.out.println("Text");` gibt Text oder Werte aus.  




## If & else 
If und else werden benutzt um eine aktion zu starten wenn etwas passiert das man vorher schon eingestellt hatt.
Für If und else braucht es eigentlich nur zwei commands.
-`if (Bedingung) { ... }`: Führt Code aus, wenn die Bedingung wahr ist
-`else { ... } `: Führt Code aus, wenn die Bedingung nicht wahr ist .

# Operatoren

- **Zuweisung**: `=` – weist einer Variablen einen Wert zu

- **Arithmetische Operatoren**:  
  `+` (Addition)  
  `-` (Subtraktion)  
  `*` (Multiplikation)  
  `/` (Division)  
  `%` (Modulo, Rest einer Division)

- **Inkrement / Dekrement**:  
  `++` (um 1 erhöhen)  
  `--` (um 1 verringern)

- **Vergleichsoperatoren**:  
  `==` (gleich)  
  `!=` (ungleich)  
  `<` (kleiner als)  
  `>` (größer als)  
  `<=` (kleiner oder gleich)  
  `>=` (größer oder gleich)

- **Logische Operatoren**:  
  `&&` (logisches UND)  
  `||` (logisches ODER)  
  `!` (logische Negation)

- **Zuweisungsoperatoren kombiniert**:  
  `+=` (Addition und Zuweisung)  
  `-=` (Subtraktion und Zuweisung)  
  `*=` (Multiplikation und Zuweisung)  
  `/=` (Division und Zuweisung)  
  `%=` (Modulo und Zuweisung)

# Arrays
Ein Array in Java ist eine Sammlung von Elementen gleichen Datentyps, die in einer festen Reihenfolge gespeichert werden.  
Arrays haben eine **feste Länge**, die bei der Erstellung festgelegt wird und nicht mehr geändert werden kann.  
Der Zugriff auf einzelne Elemente erfolgt über einen **Index**, beginnend bei `0` für das erste Element und `array.length - 1` für das letzte Element.  

## wichtigste Commands
- **Länge ermitteln**: `<Datentyp> lastElement = arr[arr.length - 1];` – gibt die Anzahl der Elemente im Array zurück

- **Erstes Element**: `arr[0]` – greift auf das erste Element zu

- **Letztes Element**: `arr[arr.length - 1]` – greift auf das letzte Element zu

- **Hinten anfügen** (ArrayList): `list.add(element)` – fügt ein Element am Ende hinzu

- **Vorne hinzufügen** (ArrayList): `list.add(0, element)` – fügt ein Element am Anfang hinzu

- **Letztes Element entfernen** (ArrayList): `list.remove(list.size() - 1)` – entfernt das letzte Element

- **Neues Array erstellen** : `int[] name = new int[10];`

## Meine Notizen
Mit Arrays kann man sich ein paar Variablen sparen.




# Loops

## for-Schleife
Die for-Schleife verwendet einen ganzzahligen Zähler, welcher sich so lange erhöht, bis das Ende erreicht ist. Eine Wiederholung des Codes innerhalb der Schleife wird "Iteration" genannt.

for (int i = 0; i < 10; i++) {
    System.out.println(i);
}
int i = 0: Erstellt den Zähler mit einem Anfangswert.
i < 10: Bedingung, welche vor jeder Iteration geprüft wird. Falls diese Bedinung false ist, wird die Schleife abgebrochen.
i++: Wird nach jeder Iteration ausgeführt und erhöht den Wert von i um 1.
i++; ist eine Kurzschreibweise für i = i + 1;.



# Methoden

greet
add
parameter

