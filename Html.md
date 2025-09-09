---
title: Html
created: '2025-09-01T06:16:22.679Z'
modified: '2025-09-08T10:54:57.120Z'
---

# Html

HTML (Hypertext Markup Language) ist die Grundsprache des Webs.  
Sie wird verwendet, um **Webseiten zu strukturieren** und deren Inhalte für Webbrowser verständlich zu machen. Mit HTML legst du fest, welche Elemente auf der Seite erscheinen – z. B. Überschriften, Absätze, Listen, Bilder, Links oder Tabellen.  

HTML selbst definiert nur die **Struktur und den Inhalt**, nicht das Aussehen. Das Design wird später durch CSS (Cascading Style Sheets) hinzugefügt, und Interaktivität durch JavaScript.  

Jedes HTML-Dokument beginnt mit dem `<html>`-Tag und enthält zwei Hauptbereiche:  

- `<head>`: Hier kommen Metainformationen rein, z. B. der Titel der Webseite, Verlinkungen zu CSS-Dateien oder andere Einstellungen für den Browser.  
- `<body>`: Hier steht der sichtbare Inhalt der Webseite, wie Texte, Bilder, Links und Listen.  

HTML-Dokumente bestehen aus **Tags**, die die Bedeutung und Struktur der Inhalte definieren. Viele Tags haben **Attribute**, die zusätzliche Informationen liefern, z. B. die Quelle eines Bildes (`src`) oder den Ziel-Link (`href`).  

Dank HTML können Webbrowser die Inhalte korrekt anzeigen und Suchmaschinen die Seiten besser verstehen. Es ist daher die **Grundlage jeder Webseite** und ein essenzielles Werkzeug für Webentwicklung.  
___
**Wichtigste commands**
- `<html>`: Start/Ende eines HTML-Dokuments  
- `<head>`: Bereich für Metainformationen der Webseite  
- `<title>`: Titel der Webseite (Browser-Tab)  
- `<body>`: Sichtbarer Inhalt der Webseite  
- `<h1>`–`<h6>`: Überschriften  
- `<p>`: Absatz/Textblock  
- `<ul>`: Ungeordnete Liste  
- `<ol>`: Geordnete Liste  
- `<li>`: Listeneintrag  
- `<a>`: Link zu einer anderen Seite  
- `<img>`: Bild einfügen  
- `<div>`: Block-Container  
- `<span>`: Inline-Container  
- `<br>`: Zeilenumbruch  
- `<hr>`: Horizontale Linie  
- `<form>`: Formular  
- `<input>`: Eingabefeld im Formular  
- `<button>`: Schaltfläche  
- `<table>`: Tabelle  
- `<tr>`: Tabellenzeile  
- `<td>`: Tabellenzelle  
- `<th>`: Tabellenkopf  
- `<meta>`: Metainformationen (Charset, Viewport)  
- `<link>`: Verbindung zu CSS oder anderen Ressourcen  
- `<script>`: JavaScript einbinden  

**Wichtige Attribute:**  
- `src`: Quelle für Bilder oder Skripte  
- `alt`: Alternativtext für Bilder  
- `href`: Ziel-URL für Links  
- `width` / `height`: Größe von Bildern oder Elementen  
- `id`: Eindeutige Kennung  
- `class`: Klassenzuordnung für CSS  

```html
<html>
  <head>
    <title>Meine Webseite</title>
  </head>
  <body>
    <h1>Willkommen!</h1>
    <p>Dies ist ein einfacher HTML-Textblock.</p>

    <h2>Liste</h2>
    <ul>
      <li>Punkt 1</li>
      <li>Punkt 2</li>
    </ul>

    <h2>Bild & Link</h2>
    <img src="images/mr-fresh.jpg" alt="Eine Katze" width="200" height="120" />
    <a href="https://developer.mozilla.org">Mehr Infos</a>
  </body>
</html>
```
