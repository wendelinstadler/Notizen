---
title: HTTP
created: '2025-11-03T13:43:44.669Z'
modified: '2025-11-03T14:03:03.482Z'
---

# HTTP

**HTTP** ist das grundlegende Protokoll für die Datenübertragung im Internet. Es regelt, wie Clients (z. B. Browser) und Server Daten austauschen, oft im JSON-Format.

## Aufbau einer URL


protokoll://host:[port]/[pfad][?parameter]


**Beispiele:**

- Minimal gültig: `https://google.com/`
- Mit Port: `https://localhost:8080/`
- Mit Pfad: `https://localhost/pfad/zu/ressource`
- Mit Parametern: `https://localhost?name=Walt&age=52`
- Alles kombiniert: `https://localhost:8080/pfad/zu/ressource?name=Walt&age=52`

## HTTP-Methoden

- **GET:** Daten vom Server abrufen
- **POST:** Neue Ressourcen auf dem Server erstellen
- **PUT:** Vorhandene Ressourcen aktualisieren
- **DELETE:** Ressourcen auf dem Server löschen

## Status Codes

- **100–199:** Information
- **200–299:** Erfolg (z. B. 200 OK)
- **300–399:** Weiterleitung (Redirect)
- **400–499:** Clientfehler (z. B. 404 Not Found)
- **500–599:** Serverfehler (z. B. 500 Internal Server Error)

---

# CSS – Gestaltung von Webseiten

**CSS** (Cascading Style Sheets) steuert das Aussehen und Layout einer Webseite. Es ermöglicht zentrale Gestaltung von Farben, Schriftarten, Abständen, Positionen und mehr.

## Einbindungsmöglichkeiten

- **Inline:** Direkt im HTML-Tag  
  `<p style="color:red;">Text</p>`
- **Intern:** Im `<style>`-Tag im `<head>`
- **Extern:** In einer `.css`-Datei:  
  `<link rel="stylesheet" href="style.css">`

## CSS-Selektoren

- `*` → Alle Elemente
- `element` → Alle Elemente dieses Typs (z. B. `p`)
- `.klasse` → Alle Elemente mit dieser Klasse
- `#id` → Element mit bestimmter ID
- `element, element` → Mehrere Elemente
- `element element` → Nachfahren-Elemente
- `element > element` → Direktes Kind
- `element:first-child`, `element:last-child` → Erstes/letztes Kind
- `element:hover` → Beim Überfahren mit der Maus
- `[attribut]` → Elemente mit Attribut
- `[attribut="wert"]` → Elemente mit bestimmtem Attributwert

## Wichtige CSS-Eigenschaften

**Text:**  
- `color`, `font-size`, `font-family`, `font-weight`, `text-align`, `text-decoration`, `text-transform`, `line-height`, `letter-spacing`

**Hintergrund & Rahmen:**  
- `background-color`, `background-image`, `background-size`, `border`, `border-radius`, `box-shadow`, `opacity`

**Layout & Box-Modell:**  
- `margin`, `padding`, `width`, `height`, `display`, `position`, `top/right/bottom/left`, `z-index`, `overflow`

**Flexbox & Grid:**  
- `flex`, `flex-direction`, `justify-content`, `align-items`
- `grid`, `grid-template-columns`, `grid-template-rows`, `gap`

**Effekte & Animationen:**  
- `transition`, `transform`, `animation`, `filter`, `cursor`

## Beispiel: Einfaches CSS

```html
<!DOCTYPE html>
<html>
<head>
  <title>CSS Beispiel</title>
  <style>
    body { background-color: #f0f0f0; font-family: Arial, sans-serif; }
    h1 { color: #3333cc; text-align: center; }
    p { color: #666666; font-size: 16px; margin: 10px 0; }
    .highlight { background-color: yellow; padding: 5px; }
    #footer { text-align: center; font-size: 12px; color: #999999; }
  </style>
</head>
<body>
  <h1>Willkommen auf meiner Webseite!</h1>
  <p>Dies ist ein <span class="highlight">Text mit Highlight</span>.</p>
  <div id="footer">© 2025 Meine Webseite</div>
</body>
</html>
