---
attachments: [Clipboard_2025-09-15-08-52-36.png]
title: Document Object Model (DOM)
created: '2025-09-09T11:18:19.707Z'
modified: '2025-09-15T06:52:36.472Z'
---

# Document Object Model (DOM)
Das **DOM** (Document Object Model) ist die Schnittstelle, mit der JavaScript auf eine Webseite zugreifen und sie verändern kann.  
Eine HTML-Seite wird vom Browser als **Baumstruktur** dargestellt:  
- Die Wurzel ist `<html>`  
- Darunter befinden sich `<head>` und `<body>`  
- Jedes Element (Überschrift, Absatz, Bild, Button, etc.) ist ein **Knoten** (Node)  

JavaScript kann diesen Baum **lesen, verändern, hinzufügen oder löschen**.  
So werden Webseiten **dynamisch und interaktiv**.
![](@attachment/Clipboard_2025-09-15-08-52-36.png)

---

## **DOM-Zugriff**

- `document.getElementById("id")` → Holt ein Element per ID  
- `document.getElementsByClassName("class")` → Holt alle Elemente mit einer Klasse  
- `document.getElementsByTagName("tag")` → Holt alle Elemente eines Typs (z. B. `p`)  
- `document.querySelector("selector")` → Holt das erste Element, das auf den CSS-Selektor passt  
- `document.querySelectorAll("selector")` → Holt alle passenden Elemente  

---

## **Eigenschaften von DOM-Elementen**

- `element.innerHTML` → Holt/ändert den HTML-Inhalt  
- `element.textContent` → Holt/ändert nur den Text  
- `element.value` → Wert von Eingabefeldern  
- `element.style.property = "value"` → CSS-Stil ändern (z. B. `element.style.color = "red";`)  
- `element.classList.add("className")` → Klasse hinzufügen  
- `element.classList.remove("className")` → Klasse entfernen  
- `element.classList.toggle("className")` → Klasse umschalten  
- `element.setAttribute("attr", "value")` → Attribut setzen  
- `element.getAttribute("attr")` → Attribut auslesen  
- `element.removeAttribute("attr")` → Attribut entfernen  

---

## **DOM-Elemente erstellen und einfügen**

- `document.createElement("tag")` → Neues Element erzeugen  
- `document.createTextNode("Text")` → Textknoten erzeugen  
- `parent.appendChild(child)` → Neues Element am Ende einfügen  
- `parent.insertBefore(newEl, refEl)` → Vor einem anderen Element einfügen  
- `parent.removeChild(child)` → Element entfernen  
- `element.replaceChild(newEl, oldEl)` → Element ersetzen  

---

## **Events im DOM**

- `element.addEventListener("click", function)` → Reagiert auf Klick  
- `element.addEventListener("mouseover", function)` → Reagiert auf Mouseover  
- `element.addEventListener("keyup", function)` → Reagiert auf Tastatureingaben  
- `element.removeEventListener("event", function)` → Event entfernen  

Häufige Events:  
- `click` → Klick  
- `dblclick` → Doppelklick  
- `mouseover` / `mouseout` → Maus rein/raus  
- `keydown` / `keyup` → Taste gedrückt/losgelassen  
- `submit` → Formular abgeschickt  
- `change` → Eingabefeld geändert  
- `load` → Seite/Element geladen  

---

## **Beispiel: DOM in Aktion**

```html
<!DOCTYPE html>
<html>
<head>
  <title>DOM Beispiel</title>
  <style>
    .highlight { color: red; font-weight: bold; }
  </style>
</head>
<body>
  <h1 id="title">Hallo Welt</h1>
  <button id="btn">Klick mich!</button>
  <ul id="list">
    <li>Eintrag 1</li>
    <li>Eintrag 2</li>
  </ul>

  <script>
    const title = document.getElementById("title");
    const button = document.getElementById("btn");
    const list = document.getElementById("list");

    // Button-Klick verändert den Titel
    button.addEventListener("click", () => {
      title.classList.toggle("highlight");

      // Neues Listenelement hinzufügen
      const newItem = document.createElement("li");
      newItem.textContent = "Neuer Eintrag";
      list.appendChild(newItem);
    });
  </script>
</body>
</html>
