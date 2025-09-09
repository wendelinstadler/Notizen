---
title: Java Script
created: '2025-09-09T11:02:55.119Z'
modified: '2025-09-09T11:05:49.070Z'
---

# Java Script

JavaScript (JS) ist die Programmiersprache des Webs, mit der Webseiten **interaktiv** und dynamisch werden.  
Während HTML die Struktur liefert und CSS das Design, sorgt JavaScript dafür, dass Elemente auf der Seite reagieren – z. B. Buttons anklickbar sind, Inhalte sich ändern oder Animationen ablaufen.

JS kann direkt in HTML eingebunden werden:  
- **Inline:** direkt im Tag (`onclick="alert('Hallo!')"`).  
- **Intern:** im `<script>`-Tag im `<head>` oder `<body>`.  
- **Extern:** über `.js`-Datei (`<script src="script.js"></script>`).

---
## Commands

---

## **Variablen & Operatoren**
- `let x = 5;` → Variable mit Blockscope  
- `const y = 10;` → Konstante  
- `var z = 20;` → Alte Variable  
- `+`, `-`, `*`, `/`, `%` → Rechenoperationen  
- `++`, `--` → Inkrement / Dekrement  
- `==`, `===`, `!=`, `!==`, `>`, `<`, `>=`, `<=` → Vergleichsoperatoren  
- `&&`, `||`, `!` → Logische Operatoren  

---

## **Arrays & Methoden**
- `array.push(value)` → Element hinzufügen  
- `array.pop()` → Letztes Element entfernen  
- `array.shift()` → Erstes Element entfernen  
- `array.unshift(value)` → Element am Anfang hinzufügen  
- `array.length` → Länge des Arrays  
- `array.includes(value)` → Prüft, ob Wert enthalten ist  
- `array.indexOf(value)` → Index eines Wertes  
- `array.slice(start, end)` → Teil-Array erstellen  
- `array.splice(index, count, ...items)` → Elemente entfernen/ersetzen  
- `array.forEach(func)` → Iteration über Elemente  
- `array.map(func)` → Neues Array durch Funktion erstellen  
- `array.filter(func)` → Array nach Bedingung filtern  
- `array.reduce(func, initial)` → Array zu einem Wert reduzieren  

---

## **Strings & Methoden**
- `str.length` → Länge des Strings  
- `str.toUpperCase()` → Großbuchstaben  
- `str.toLowerCase()` → Kleinbuchstaben  
- `str.includes(substring)` → Prüfen auf Teilstring  
- `str.indexOf(substring)` → Index des Teilstrings  
- `str.slice(start, end)` → Teilstring extrahieren  
- `str.replace("alt", "neu")` → Text ersetzen  
- `str.split("delimiter")` → String in Array aufteilen  
- `str.trim()` → Leerzeichen entfernen  

---

## **DOM & Events**
- `document.getElementById("id")` → Element per ID  
- `document.getElementsByClassName("class")` → Elemente per Klasse  
- `document.querySelector("selector")` → Erstes passendes Element  
- `document.querySelectorAll("selector")` → Alle passenden Elemente  
- `element.innerHTML` → Inhalt ändern  
- `element.textContent` → Textinhalt ändern  
- `element.style.property = "value"` → CSS-Stil ändern  
- `element.setAttribute("attr", "value")` → Attribut setzen  
- `element.addEventListener("click", func)` → Eventlistener hinzufügen  
- `element.removeEventListener("click", func)` → Eventlistener entfernen  

---

## **Funktionen**
- `function name(params) { ... }` → Klassische Funktion  
- `const name = (params) => { ... }` → Pfeilfunktion  
- `return` → Wert aus Funktion zurückgeben  
- `arguments` → Zugriff auf alle übergebenen Argumente  

---

## **Timing & Intervalle**
- `setTimeout(func, ms)` → Einmalige Verzögerung  
- `setInterval(func, ms)` → Wiederholende Ausführung  
- `clearTimeout(id)` → Timeout stoppen  
- `clearInterval(id)` → Intervall stoppen  

---

## **Konsole & Debugging**
- `console.log(value)` → Ausgabe in der Konsole  
- `console.error(value)` → Fehlermeldung  
- `console.warn(value)` → Warnung  
- `console.table(array)` → Array/Objekt als Tabelle anzeigen  

---

## **Mathematik & Zufall**
- `Math.random()` → Zufallszahl 0–1  
- `Math.floor(num)` → Abrunden  
- `Math.ceil(num)` → Aufrunden  
- `Math.round(num)` → Runden  
- `Math.max(a,b,...)` → Maximalwert  
- `Math.min(a,b,...)` → Minimalwert  
- `Math.abs(num)` → Absolutwert  
- `Math.sqrt(num)` → Quadratwurzel  

---

## **JSON & Local Storage**
- `JSON.parse(jsonString)` → JSON-Text in Objekt  
- `JSON.stringify(object)` → Objekt in JSON-Text  
- `localStorage.setItem("key", value)` → Wert speichern  
- `localStorage.getItem("key")` → Wert auslesen  
- `localStorage.removeItem("key")` → Wert löschen  
- `localStorage.clear()` → Alle Werte löschen  

---

## **Bedingungen & Kontrolle**
- `if (condition) { ... } else { ... }`  
- `switch(variable) { case value: ... break; default: ... }`  
- `?:` → Ternary Operator, z. B. `let result = (x > 0) ? "Positiv" : "Negativ";`



## **Beispiel: Einfaches JavaScript**

```html
<!DOCTYPE html>
<html>
<head>
  <title>JavaScript Beispiel</title>
  <style>
    button { padding: 10px 20px; margin: 10px; }
  </style>
</head>
<body>
  <h1>Willkommen!</h1>
  <p id="text">Klicke auf den Button:</p>
  <button id="btn">Klick mich!</button>

  <script>
    const button = document.getElementById("btn");
    const text = document.getElementById("text");

    button.addEventListener("click", () => {
      text.innerHTML = "Der Button wurde geklickt!";
      text.style.color = "blue";
      console.log("Button geklickt!");
    });

    // Variable Beispiel
    let count = 0;
    button.addEventListener("click", () => {
      count++;
      console.log("Anzahl Klicks:", count);
    });
  </script>
</body>
</html>
