---
title: CSS
created: '2025-09-08T06:21:49.074Z'
modified: '2025-09-09T11:10:10.115Z'
---

# CSS

CSS (Cascading Style Sheets) ist die Sprache, mit der du das **Aussehen und Layout** einer Webseite gestaltest.  
Während HTML die **Struktur** liefert, sorgt CSS dafür, dass die Inhalte **schön aussehen** – z. B. Farben, Schriftarten, Abstände, Größen, Positionen und Hintergründe.  

Mit CSS kannst du das Design einer Webseite **einheitlich und flexibel** gestalten. Änderungen lassen sich zentral durchführen, ohne dass der HTML-Code jedes Mal angepasst werden muss.  

CSS wird in drei Varianten eingebunden:  
- **Inline:** direkt im HTML-Tag (`<p style="color:red;">Text</p>`)  
- **Intern:** innerhalb eines `<style>`-Tags im `<head>`  
- **Extern:** in einer separaten `.css`-Datei, die über `<link rel="stylesheet" href="style.css">` eingebunden wird  

---
## **CSS-Selektoren**

- `*` → Alle Elemente  
- `element` → Alle Elemente eines Typs (z. B. `p`)  
- `.class` → Alle Elemente mit dieser Klasse  
- `#id` → Element mit bestimmter ID  
- `element, element` → Mehrere Elemente gleichzeitig  
- `element element` → Kind-Elemente  
- `element > element` → Direktes Kind  
- `element:first-child`, `element:last-child` → Erstes / letztes Kind  
- `element:hover` → Element bei Hover  
- `[attribute]` → Elemente mit einem Attribut  
- `[attribute="value"]` → Elemente mit bestimmtem Attributwert  

---

## **CSS-Eigenschaften**

**Text & Schrift:**  
- `color` → Textfarbe  
- `font-size` → Schriftgröße  
- `font-family` → Schriftart  
- `font-weight` → Schriftstärke  
- `text-align` → Textausrichtung  
- `text-decoration` → Unterstrichen, durchgestrichen etc.  
- `text-transform` → Groß-/Kleinschreibung  
- `line-height` → Zeilenhöhe  
- `letter-spacing` → Zeichenabstand  

**Hintergrund & Rahmen:**  
- `background-color` → Hintergrundfarbe  
- `background-image` → Hintergrundbild  
- `background-size` → Größe des Hintergrundbilds  
- `border` → Rahmen  
- `border-radius` → Runde Ecken  
- `box-shadow` → Schatten für Elemente  
- `opacity` → Transparenz  

**Layout & Box-Modell:**  
- `margin` → Außenabstand  
- `padding` → Innenabstand  
- `width` / `height` → Breite / Höhe  
- `display` → block, inline, flex, grid  
- `position` → static, relative, absolute, fixed, sticky  
- `top`, `right`, `bottom`, `left` → Positionierung  
- `z-index` → Ebenenreihenfolge  
- `overflow` → hidden, scroll, auto  

**Flexbox & Grid:**  
- `flex`, `flex-direction`, `justify-content`, `align-items` → Flexbox-Layout  
- `grid`, `grid-template-columns`, `grid-template-rows` → Grid-Layout  
- `gap` → Abstand zwischen Flex/Grid-Items  

**Effekte & Animationen:**  
- `transition` → sanfte Übergänge  
- `transform` → verschieben, skalieren, drehen  
- `animation` → Keyframe-Animationen  
- `filter` → blur, grayscale, brightness  
- `cursor` → Mauszeiger-Stil# HTML & CSS – Kommandos / Tags / Eigenschaften

---

## Beispiel: Einfaches CSS

```html
<!DOCTYPE html>
<html>
<head>
  <title>CSS Beispiel</title>
  <style>
    body {
      background-color: #f0f0f0;
      font-family: Arial, sans-serif;
    }

    h1 {
      color: #3333cc;
      text-align: center;
    }

    p {
      color: #666666;
      font-size: 16px;
      margin: 10px 0;
    }

    .highlight {
      background-color: yellow;
      padding: 5px;
    }

    #footer {
      text-align: center;
      font-size: 12px;
      color: #999999;
    }
  </style>
</head>
<body>
  <h1>Willkommen auf meiner Webseite!</h1>
  <p>Dies ist ein <span class="highlight">Text mit Highlight</span>.</p>
  <div id="footer">© 2025 Meine Webseite</div>
</body>
</html>
```
