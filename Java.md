---
title: Java
created: '2025-08-07T09:11:57.638Z'
modified: '2025-08-08T07:13:40.189Z'
---

# Java

Java ist eine objektorientierte Programmiersprache, die weltweit sehr verbreitet ist.  
Sie ist bekannt für ihre Plattformunabhängigkeit, weil Java-Programme nicht direkt als Maschinencode ausgeführt werden,  
sondern zuerst in **Bytecode** kompiliert werden. Dieser Bytecode läuft dann auf der **Java Virtual Machine (JVM)**,  
die es für fast jedes Betriebssystem gibt.  

Das macht Java besonders geeignet für Anwendungen, die auf verschiedenen Geräten und Systemen laufen sollen –  
von Desktop-Programmen über Web-Anwendungen bis hin zu Apps für Android.

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

---

## Beispielcode

```java
public class Main {
    public static void main(String[] args) {
        // Variable mit Datentyp int erstellen und Wert zuweisen
        int number = 10;

        // Wert auf der Konsole ausgeben
        System.out.println(number);
    }
}

