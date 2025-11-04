---
title: Spring controller
created: '2025-11-04T12:48:39.767Z'
modified: '2025-11-04T12:53:14.047Z'
---

## Spring controller
 
 
### 1. Was ist ein Controller in Spring?
 
Verwaltet HTTP-Anfragen (GET, POST, etc.)
 
Antwortet auf Anfragen mit Daten (z. B. Strings, Objekte, JSON)
 
Annotation:

@RestController
 
 
Kennzeichnet eine Klasse als REST-Controller
 
### 2. HTTP-Endpunkte definieren

GET-Anfrage:

- `@GetMapping("/hello")`
 
 
Wird bei einer GET-Anfrage an /hello ausgeführt
 
POST-Anfrage:

@PostMapping("/create")
 
 
Für Daten, die gesendet werden (z. B. JSON)
 
📌 Weitere Methoden:
 
@PutMapping → Aktualisieren
 
@DeleteMapping → Löschen
 
###   3. Pfadvariablen verwenden

@GetMapping("/user/{id}")

public String getUser(@PathVariable int id)
 
 
Liest id direkt aus der URL, z. B. /user/5
 
Gut für eindeutige Ressourcen
 
### ✅ 4. Anfrageparameter verwenden

@GetMapping("/search")

public String search(@RequestParam String keyword)
 
 
Liest Parameter aus der URL, z. B. /search?keyword=java
 
Gut für Filter, Suche, Optionen
 
### ✅ 5. Anfragekörper verarbeiten

@PostMapping("/message")

public void create(@RequestBody Message msg)
 
 
Verarbeitet JSON im Body der Anfrage
 
Konvertiert automatisch zu Java-Objekt
 
📌 Beispielklasse:

public record Message(String content) {}
 
### ✅ 6. Rückgabewerte
 
Methoden können Strings, Objekte, Listen usw. zurückgeben
 
Spring wandelt alles automatisch in JSON um
 
return new User("Alice", 30);
 
📌 Beispielklasse:

record User(String name, int age) {}
 
### ✅ 7. Gemeinsamer Pfad für alle Methoden

@RequestMapping("/api")

@RestController

public class MyController
 
 
Alle Methoden in der Klasse beginnen automatisch mit /api
 
### ✅ 8. Server starten & testen
 
Server läuft auf:
http://localhost:8080
 
Testen z. B. mit Hoppscotch:
 
Browsererweiterung installieren
 
http://localhost freigeben
 
