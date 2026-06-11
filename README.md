# Unser Gemeinschaftskochbuch

Ein kollaboratives Hugo-Kochbuch, in dem jeder seine Lieblingsrezepte teilen kann.

## Rezept beisteuern

1. Eine neue `.md`-Datei in `content/recipes/` erstellen mit einem URL-freundlichen Dateinamen (z.B. `mein-rezept.md`)
2. Die Vorlage unten für das Front Matter verwenden
3. Den Rezeptinhalt im Hauptteil schreiben
4. Über einen Pull-Request einreichen!

### Rezeptvorlage

```markdown
---
title: "Name des Rezepts"
date: 2026-06-11
draft: false
description: "Eine kurze Beschreibung des Gerichts"
categories: ["Kategorie"]
tags: ["schlagwort1", "schlagwort2"]
contributors: ["Dein Name"]
servings: 4
prep_time: "15 Min."
cook_time: "30 Min."
ingredients:
  - "1 Tasse Zutat"
  - "2 EL Zutat"
instructions:
  - "Schritt 1: Etwas tun"
  - "Schritt 2: Etwas anderes tun"
difficulty: "Einfach"
---

## Über dieses Rezept

Erzähle die Geschichte hinter deinem Rezept!
```

### Schwierigkeitsstufen

- `Einfach` - Anfängerfreundlich, unter 30 Minuten
- `Mittel` - Etwas Technik erforderlich
- `Schwierig` - Fortgeschritten, erfordert Übung

### Verfügbare Kategorien

Erstelle whatever Kategorien für dein Rezept sinnvoll sind! Einige Beispiele:
- Frühstück, Hauptgericht, Dessert, Suppe, Salat, Vorspeise, Beilage, Snack
- Italienisch, Indisch, Japanisch, Mexikanisch, Französisch, Thai, usw.

## Lokal ausführen

```bash
hugo server -D
```

Dann http://localhost:1313 im Browser öffnen.

## Build erstellen

```bash
hugo
```

Die statische Website wird im Verzeichnis `public/` generiert.

## Projektstruktur

```
content/
  recipes/          # Alle Rezept-.md-Dateien kommen hier rein
layouts/
  recipes/          # Benutzerdefinierte Rezeptvorlagen
  partials/         # Theme-Overrides
assets/
  css/              # Benutzerdefinierte Stile
themes/
  PaperMod/         # Hugo-Theme (Git-Submodul)
```