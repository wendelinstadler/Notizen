---
title: Dateisystem
created: '2025-08-07T09:06:25.013Z'
modified: '2025-08-07T12:26:01.438Z'
---

# Dateisystem

## Recherche

- Was ist ein Systempfad?

Der der aufgezeichnete Weg der aufzeigt wie man zur Datei gekommen ist.

- Welche Arten von Systempfaden gibt es? Was sind die Unterschiede?

Der Relative und der absolute. Der absolute zeigt jeden Schritt und der relative zeigt es nur von dort wo man gestartet ist.

## Pfade angeben

Gegeben sei folgendes Dateisystem.

```
0  C:\
1  └── user\
2      ├── documents\
3      │   ├── resume.pdf
4      │   └── report.docx
5      ├── music\
6      │   ├── rock\
7      │   │   └── queen.mp3
8      |   └── rap\
9      │       └── kendrick.mp3
10     ├── photos\
11     │   ├── vacation\
12     │   │   └── beach.png
13     │   └── birthday\
14     │       └── party.jpg
15     └── scripts\
16         └── backup.sh
```

- Gib den absoluten Pfad der Datei auf Zeile 4 an.
C:\user\documents\resume.pdf\report.docx
- Gib den absoluten Pfad der Datei auf Zeile 9 an.
C:\user\music\rap\kendrick.mp3
- Gib den absoluten Pfad der Datei auf Zeile 12 an.
C:\user\photos\vacation\beach.png
- Gib den absoluten Pfad der Datei auf Zeile 16 an.
C:\user\scripts\backup.sh

- Gib den relativen Pfad der Datei auf Zeile 3 an, ausgehend vom Verzeichnis auf Zeile 15.
..\documents\resume.pdf
- Gib den relativen Pfad der Datei auf Zeile 7 an, ausgehend vom Verzeichnis auf Zeile 11. (Ich habe es falsch gelesen und umgekehrt gemacht.)
..\..\..\photos\vacation
- Gib den relativen Pfad der Datei auf Zeile 14 an, ausgehend vom Verzeichnis auf Zeile 6.
..\..\..\music\rock
- Gib den relativen Pfad der Datei auf Zeile 16 an, ausgehend vom Verzeichnis auf Zeile 2.
..\..\documents
## Notizen

Beim relativen startet man dort wo man schon ist und beim absoluten von ganz am Anfang.
Wenn man einen Ordner zurück gehen will muss man ..\ machen.
