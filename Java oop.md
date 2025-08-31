---
title: Java oop
created: '2025-08-19T09:24:51.761Z'
modified: '2025-08-31T19:21:35.487Z'
---


# Java oop

Java verwendet objektorientierte Programmierung, kurz OOP. Dabei gibt es Klassen als Baupläne und Objekte als konkrete Dinge.
Die vier Grundideen sind: Kapselung, um Daten zu schützen, Vererbung, damit Klassen Eigenschaften übernehmen können, Polymorphismus,
damit gleiche Methoden unterschiedlich umgesetzt werden können,und Abstraktion, damit nur das Wichtige sichtbar ist.
Dadurch wird der Code übersichtlich, wiederverwendbar und leicht erweiterbar.

# Objekte und Klassen
Objektorientierte Programmierung (OOP) ist ein Prinzip, das uns hilft, komplexe Programme zu strukturieren und zu organisieren. Ein zentrales Konzept in der OOP sind Klassen und Objekte.

  - Eine Klasse ist wie eine Bauplan oder Vorlage für Objekte. Sie definiert, welche Eigenschaften (Variablen) und Methoden (Funktionen) ein Objekt haben wird.
  - Ein Objekt ist eine Instanz einer Klasse. Es hat Eigenschaften, die durch Variablen repräsentiert werden, und kann Aktionen durch Methoden ausführen.

## Wichtige Java-Kommandos / Keywords
- `class` → Definiert eine Klasse
- `new` → Erzeugt ein Objekt
- `public` → Zugriffsmodifikator, sichtbar für alle
- `private` → Zugriffsmodifikator, nur innerhalb der Klasse sichtbar
- `void` → Methode ohne Rückgabewert
- `return` → Gibt einen Wert aus einer Methode zurück
- `this` → Referenz auf das aktuelle Objekt
- `Konstruktor` → Spezielle Methode zur Initialisierung eines Objekts

## Beispiel: Klasse, Objekt und Konstruktor

```java
// Klasse definieren
public class Car {
    String color; // Eigenschaft
    int speed;    // Eigenschaft

    // Konstruktor
    public Car(String color, int speed) {
        this.color = color;
        this.speed = speed;
    }

    // Methode
    public void drive() {
        System.out.println("Das " + color + "e Auto fährt mit " + speed + " km/h.");
    }
}

// Verwendung der Klasse
public class Main {
    public static void main(String[] args) {
        Car myCar = new Car("Rot", 120); // Objekt erstellen mit Konstruktor
        myCar.drive(); // Ausgabe: Das Rote Auto fährt mit 120 km/h.

        Car anotherCar = new Car("Blau", 80);
        anotherCar.drive(); // Ausgabe: Das Blaue Auto fährt mit 80 km/h.
    }
}
```

# Instanzmethoden
Eine **Instanzmethode** gehört immer zu einem **Objekt** und kann auf dessen Eigenschaften zugreifen.  
Sie wird ohne `static` deklariert und muss über ein **Objekt der Klasse** aufgerufen werden.  
Mit `this` kann man innerhalb der Methode auf das aktuelle Objekt zugreifen.  

```java
public class Car {
    int speed; // Eigenschaft des Objekts

    // Instanzmethode
    public void drive() {
        // 'this.speed' referenziert die Geschwindigkeit des aktuellen Objekts
        System.out.println("Das Auto fährt mit " + this.speed + " km/h.");
    }
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car();   // Objekt erstellen
        myCar.speed = 100;       // Eigenschaft des Objekts setzen
        myCar.drive();           // Instanzmethode aufrufen -> Ausgabe: Das Auto fährt mit 100 km/h.

        Car anotherCar = new Car();
        anotherCar.speed = 80;
        anotherCar.drive();      // Jede Instanz hat eigene Eigenschaften -> Ausgabe: Das Auto fährt mit 80 km/h.
    }
}
```
# Konstruktor
Ein **Konstruktor** ist eine spezielle Methode einer Klasse, die automatisch aufgerufen wird, wenn ein **Objekt** erstellt wird.  
Er hat **den gleichen Namen wie die Klasse** und keinen Rückgabewert.  
Konstruktoren werden genutzt, um die **Eigenschaften eines Objekts direkt beim Erstellen zu initialisieren**.  
Man kann mehrere Konstruktoren in einer Klasse haben (Überladung), um Objekten verschiedene Startwerte zu geben.

---

## Beispiel

```java
public class Car {
    String color;
    int speed;

    // Konstruktor
    public Car(String color, int speed) {
        this.color = color; // Initialisierung der Eigenschaften
        this.speed = speed;
    }

    public void drive() {
        System.out.println("Das " + color + "e Auto fährt mit " + speed + " km/h.");
    }
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car("Rot", 120);   // Konstruktor wird automatisch aufgerufen
        myCar.drive(); // Ausgabe: Das Rote Auto fährt mit 120 km/h.

        Car anotherCar = new Car("Blau", 80);
        anotherCar.drive(); // Ausgabe: Das Blaue Auto fährt mit 80 km/h.
    }
}
```

# Testing
Tests sind ein wichtiger Bestandteil der Softwareentwicklung.  
Sie helfen, die **Funktionalität, Qualität und Stabilität** von Code sicherzustellen.  
Durch Tests können Fehler früh erkannt und behoben werden, bevor sie in der Produktion Probleme verursachen.

---

## Wichtige Java-Kommandos: Tests

- `@Test` → Markiert eine Methode als Testmethode, die automatisch ausgeführt wird  
- `assertEquals(expected, actual)` → Prüft, ob der erwartete Wert dem tatsächlichen Wert entspricht  
- `assertTrue(condition)` → Prüft, ob eine Bedingung `true` ist  
- `assertFalse(condition)` → Prüft, ob eine Bedingung `false` ist  
- `assertThrows(Exception.class, executable)` → Prüft, ob eine bestimmte Exception geworfen wird  

---

## Setup von JUnit in IntelliJ

1. **Maven-Projekt öffnen**  
2. **JUnit-Dependency hinzufügen** in `pom.xml`:

```xml
<dependencies>  
    <dependency>
        <groupId>org.junit.jupiter</groupId>  
        <artifactId>junit-jupiter</artifactId>  
        <version>RELEASE</version>  
        <scope>test</scope>  
    </dependency>
</dependencies>
```
## Beispiel
```Java
public class Circle {
    private double radius;

    // Konstruktor zum Initialisieren des Radius
    public Circle(double radius) {
        this.radius = radius;
    }

    // Methode zur Berechnung der Kreisfläche
    public double getArea() {
        return Math.PI * radius * radius;
    }
}

import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertEquals;

public class CircleTest {

    @Test
    void getArea() {
        // Given: Vorbereitung der Testdaten / Objekt
        Circle c = new Circle(2); // Kreis mit Radius 2

        // When: Ausführung der Methode, die getestet werden soll
        double result = c.getArea();

        // Then: Überprüfung des Ergebnisses
        // Erwartetes Ergebnis: 12.56637061436
        assertEquals(12.56637061436, result); // Test schlägt fehl, wenn Ergebnis nicht passt
    }
}
```

# Test Driven Development (TDD)

**TDD** ist eine Entwicklungsstrategie, bei der **zuerst Tests geschrieben** werden, bevor der eigentliche Code implementiert wird.  
Ziel: **sauberer, getesteter und fehlerfreier Code** von Anfang an.

---

## Vorgehensweise (3 Schritte)

1. **Red** → Test schreiben, der zunächst **fehlschlägt  
2. **Green** → Nur so viel Code schreiben, dass der Test besteht  
3. **Refactor** → Code verbessern, Tests bestehen weiterhin

---

## Wichtige „Commands“ / Werkzeuge in Java

- `@Test` → Kennzeichnet eine Testmethode  
- `assertEquals(expected, actual)` → Prüft Werte  
- `assertTrue(condition)` → Prüft `true`  
- `assertFalse(condition)` → Prüft `false`  
- `assertThrows(Exception.class, executable)` → Prüft Exception  

---

## Beispiel: TDD in Java

```java
// Test zuerst schreiben
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertEquals;

public class CalculatorTest {

    @Test
    void testAdd() {
        Calculator calc = new Calculator();
        assertEquals(5, calc.add(2, 3)); // Test zuerst: 2 + 3 = 5
    }
}

// Danach die Klasse implementieren
public class Calculator {

    public int add(int a, int b) {
        return a + b; // Code nur, damit Test besteht
    }
}
```
# Referenzen

In Java speichern Variablen **nicht immer direkt die Werte**, sondern oft **Referenzen** auf die Werte.  
Eine Referenz ist wie eine **Adresse im Speicher**, die angibt, wo das eigentliche Objekt liegt.  
Wenn mehrere Variablen dieselbe Referenz haben, zeigen sie auf dasselbe Objekt, und Änderungen über eine Variable wirken sich auf alle aus, die dieselbe Referenz besitzen.

---

## Beispiel: Referenzen bei Objekten

```java
class Car {
    double maxSpeed;
}

public class Main {
    public static void main(String[] args) {
        Car toyota = new Car(); // toyota speichert die Referenz auf ein Car-Objekt
        Car bmw = toyota;       // bmw speichert dieselbe Referenz

        toyota.maxSpeed = 150;  // Änderung über toyota
        bmw.maxSpeed = 200;     // Änderung über bmw

        System.out.println(toyota.maxSpeed); // Ausgabe: 200
    }
}
```

# Enums
Enums, kurz für "Enumerations", sind spezielle Datentypen in Java, die eine Menge konstanter Werte repräsentieren. Diese Werte werden oft als Aufzählungen oder Liste von Möglichkeiten verwendet. Enums können in Java dazu beitragen, den Code lesbarer und wartbarer zu machen, indem sie eine festgelegte Menge von zulässigen Werten definieren.
## Wichtige Punkte / Commands

- `enum` → Schlüsselwort zum Erstellen eines Enums  
- `values()` → Liefert ein Array aller Enum-Werte  
- `name()` → Gibt den Namen des Enum-Werts als String zurück  
- `ordinal()` → Gibt die Position des Enum-Werts in der Definition zurück (0-basiert)

---

## Beispiel

```java
// Enum definieren
public enum Day {
    MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY
}

public class Main {
    public static void main(String[] args) {
        Day today = Day.MONDAY; // Enum-Wert zuweisen

        System.out.println("Heute ist: " + today);      // Ausgabe: Heute ist: MONDAY
        System.out.println("Position: " + today.ordinal()); // Ausgabe: Position: 0

        // Alle Enum-Werte durchlaufen
        for (Day d : Day.values()) {
            System.out.println(d);
        }
    }
}
```
# Vererbung

**Vererbung** ist ein zentrales Konzept der objektorientierten Programmierung.  
Sie ermöglicht es, **Eigenschaften und Methoden einer bestehenden Klasse (Elternklasse / Superklasse)** in einer **neuen Klasse (Kindklasse / Subklasse)** wiederzuverwenden.  
Das vermeidet doppelten Code und erleichtert die Wartung.

---

## Wichtige Commands
- `extends` → Schlüsselwort, mit dem eine Klasse von einer anderen Klasse erbt  
- `super` → Zugriff auf die Methoden/Attribute der Elternklasse oder Aufruf des Konstruktors der Elternklasse  
- `@Override` → Annotation, wenn eine Methode aus der Elternklasse überschrieben wird  
---
```Java
// Oberklasse
class Vehicle {
    double maxSpeed;
}

// Unterklasse
class Car extends Vehicle {
    int doors;
}

// Unterklasse
class Motorbike extends Vehicle {
    boolean hasSidecar;
}

public class Main {
    public static void main(String[] args) {
        Car car = new Car();
        car.maxSpeed = 180; // von Vehicle geerbt
        car.doors = 4;      // eigene Eigenschaft

        Motorbike bike = new Motorbike();
        bike.maxSpeed = 150; // von Vehicle geerbt
        bike.hasSidecar = true;

        System.out.println("Auto: " + car.maxSpeed + " km/h mit " + car.doors + " Türen");
        System.out.println("Motorrad: " + bike.maxSpeed + " km/h mit Beiwagen: " + bike.hasSidecar);
    }
}

```

# Interfaces
Java-Interfaces sind abstrakte Datentypen, die als **Schnittstellen** dienen.  
Klassen, die ein Interface implementieren, verpflichten sich dazu, die darin definierten **Methodensignaturen** umzusetzen.

Ein Interface enthält selbst keine konkrete Implementierung (außer `default`- oder `static`-Methoden).  
Dadurch können völlig unterschiedliche Klassen ein gemeinsames Verhalten garantieren, auch wenn sie **nicht in derselben Vererbungshierarchie** stehen.

## Wichtige Java-Kommandos für Interfaces

- `interface` → Definiert ein Interface  
- `implements` → Eine Klasse implementiert ein Interface  
- `extends` → Ein Interface erbt von einem anderen Interface  
- `abstract` → Methoden in Interfaces sind implizit abstrakt (außer `default`, `static`, `private`)  
- `default` → Methode mit Standard-Implementierung im Interface (seit Java 8)  
- `static` → Statische Methode im Interface (seit Java 8)  
- `private` → Private Hilfsmethoden im Interface (seit Java 9)  
- `public static final` → Alle Variablen in einem Interface sind automatisch Konstanten 
- `@Override` → Zeigt, dass eine Methode aus dem Interface überschrieben wird  
- `@FunctionalInterface` → Interface mit genau einer abstrakten Methode, kann für Lambda-Ausdrücke genutzt werden 

## Kurzes Interface-Beispiel
```
// Interface definieren
public interface Animal {
    void makeSound();
}

// Hund implementiert das Interface
public class Dog implements Animal {
    @Override
    public void makeSound() {
        System.out.println("Wuff!");
    }
}

// Verwendung
public class Main {
    public static void main(String[] args) {
        Animal dog = new Dog();
        dog.makeSound(); // Ausgabe: Wuff!
    }
}
```

# List, Set & Map

Lists, Sets und Maps sind Datenstrukturen, die uns Helfen, unsere Daten zu organisieren. Jede Struktur hat Vor- und Nachteile und die Wahl der Struktur kommt immer auf den Kontext an.
In Java gibt es drei wichtige Collection-Typen: **List**, **Set** und **Map**.  
- Eine **List** ist wie ein flexibles Array: geordnet, erlaubt Duplikate, Zugriff über einen Index.  
- Ein **Set** speichert nur eindeutige Werte: ungeordnet, keine Duplikate, kein Index.  
- Eine **Map** speichert Schlüssel-Wert-Paare: Schlüssel eindeutig, Werte können doppelt sein.  



## Commands
- `addAll` → alles hinzufügen
- `removeAll` → alles entfernen, was drin ist
- `retainAll` → alles außer dem, was drin ist, entfernen
- `containsAll` → prüfen, ob alles drin ist
- `add(element)` → Element hinzufügen (List, Set)  
- `remove(element)` → Element entfernen (List, Set)  
- `get(index)` → Element an Position abrufen (nur List)  
- `size()` → Anzahl der Elemente  
- `contains(element)` → prüft, ob enthalten (Set, List)  
- `put(key, value)` → Schlüssel-Wert-Paar hinzufügen (Map)  
- `get(key)` → Wert zu Schlüssel abrufen (Map)  
- `containsKey(key)` → prüft, ob Schlüssel enthalten ist (Map)  
- `keySet()` → alle Schlüssel abrufen (Map)  

---

## Beispielcode
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // ===== LIST =====
        List<String> shoppingList = new ArrayList<>();
        shoppingList.add("Popcorn");
        shoppingList.add("Chips");
        shoppingList.add("Avocado");
        shoppingList.add("Chips"); // Duplikate erlaubt
        System.out.println("List: " + shoppingList);
        System.out.println("Erstes Element: " + shoppingList.get(0));

        // ===== SET =====
        Set<String> students = new HashSet<>();
        students.add("Max");
        students.add("Moritz");
        students.add("Max"); // wird ignoriert
        System.out.println("Set: " + students);
        System.out.println("Enthält Max? " + students.contains("Max"));

        // ===== MAP =====
        Map<String, Double> prices = new HashMap<>();
        prices.put("Chips", 4.20);
        prices.put("Guacamole", 6.90);
        prices.put("Chips", 5.00); // überschreibt alten Wert
        System.out.println("Map: " + prices);
        System.out.println("Preis von Chips: " + prices.get("Chips"));

        // Über Map iterieren
        for (String key : prices.keySet()) {
            System.out.println("Produkt: " + key + " → Preis: " + prices.get(key));
        }
    }
}
```
# Streams
Streams bieten uns eine einfache und übersichtliche Möglichkeit, Operationen auf Collections wie List auszuführen. Dafür rufen wir die Methode stream() auf einer Instanz auf. Danach ketten wir verschiedene Operationen aneinander, um das gewünschte ergebnis zu erhalten. Folgendes Beispiel filtert die Liste zuerst, so dass nur noch gerade Zahlen übrig bleiben. Anschliessend wird jede Zahl auf der Konsole ausgegeben.

Streams arbeiten nach dem Prinzip **Pipeline**:  
1. **Zwischenoperationen** → bauen die Pipeline auf, zurück kommt immer ein Stream  
2. **Terminierende Operationen** → führen die Pipeline aus und liefern ein Ergebnis  

---

## Wichtige Commands / Methoden

### Zwischenoperationen (geben Stream zurück)
- `filter(predicate)` → filtert Elemente nach einer Bedingung  
- `map(function)` → wandelt jedes Element um  
- `distinct()` → entfernt Duplikate  
- `sorted()` → sortiert die Elemente  
- `limit(n)` → beschränkt auf die ersten n Elemente  
- `skip(n)` → überspringt die ersten n Elemente  

### Terminierende Operationen (geben kein Stream zurück)
- `forEach(consumer)` → führt Aktion für jedes Element aus  
- `reduce(identity, accumulator)` → reduziert Stream zu einem Wert  
- `count()` → Anzahl der Elemente  
- `collect(Collectors.toList())` → sammelt Elemente wieder in einer Liste  
- `anyMatch(predicate)` → prüft, ob ein Element die Bedingung erfüllt  
- `allMatch(predicate)` → prüft, ob alle Elemente die Bedingung erfüllen  
- `findFirst()` → gibt das erste Element zurück (optional)  

### Beispiel
```java
import java.util.List;

public class Main {
    public static void main(String[] args) {
        List<Integer> numbers = List.of(1, 2, 3, 4, 5);

        numbers.stream()
               .filter(n -> n % 2 == 0)      // nur gerade Zahlen
               .forEach(System.out::println); // Ausgabe: 2, 4
    }
}
```
## Mehrere Zwischenoperationen + Sammeln
```Java
import java.util.List;
import java.util.stream.Collectors;

public class Main {
    public static void main(String[] args) {
        List<Integer> numbers = List.of(1, 2, 3, 4, 5, 2, 4);

        List<Integer> result = numbers.stream()
                                      .distinct()                 // Duplikate entfernen
                                      .filter(n -> n % 2 == 0)   // gerade Zahlen
                                      .map(n -> n * n)            // quadrieren
                                      .sorted()                   // sortieren
                                      .collect(Collectors.toList()); // in Liste sammeln

        System.out.println(result); // Ausgabe: [4, 16]
    }
}
```
## Reduzieren auf Summe
```Java
import java.util.List;

public class Main {
    public static void main(String[] args) {
        List<Integer> numbers = List.of(1, 2, 3, 4, 5);

        int sum = numbers.stream()
                         .reduce(0, (a, b) -> a + b); // alle Zahlen summieren

        System.out.println(sum); // Ausgabe: 15
    }
}
```



