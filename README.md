# Unser Gemeinschaftskochbuch

Ein kollaboratives Hugo-Kochbuch, in dem jeder seine Lieblingsrezepte teilen kann — mit einem warmen, editorialen Design, Dunkelmodus, Portionen-Umrechner und Druckansicht.

## Rezept beisteuern

1. Eine neue `.md`-Datei in `content/recipes/` erstellen mit einem URL-freundlichen Dateinamen (z.B. `mein-rezept.md`). Am einfachsten mit der Vorlage:
   ```bash
   hugo new content/recipes/mein-rezept.md
   ```
2. **Ein Bild hinzufügen:** Querformat (ca. 8:5, z.B. 800×500) nach `static/images/recipes/` legen und im Front Matter unter `image:` eintragen. Ohne Bild wird automatisch ein Platzhalter angezeigt.
3. Das Front Matter ausfüllen und den Rezeptinhalt schreiben (siehe Vorlage unten).
4. `draft: false` setzen und über einen Pull-Request einreichen!

Die vier vorhandenen Rezepte dienen als Referenz dafür, wie ein fertiges Rezept aussehen soll.

### Rezeptvorlage

```markdown
---
# ── Basis ────────────────────────────────────────────────
title: "Name des Rezepts"
date: 2026-06-12
draft: false
description: "Eine kurze, appetitanregende Beschreibung (1–2 Sätze)."
image: "images/recipes/mein-rezept.jpg"

# ── Einordnung ───────────────────────────────────────────
categories: ["Hauptgericht"]
tags: ["schlagwort1", "schlagwort2"]
contributors: ["Dein Name"]
difficulty: "Einfach" # Einfach | Mittel | Schwierig

# ── Eckdaten ─────────────────────────────────────────────
servings: 4
prep_time: "15 Min."
cook_time: "30 Min."

# ── Zutaten ──────────────────────────────────────────────
# Mengenangabe an den Anfang stellen (z.B. "500g …", "2 EL …"),
# dann funktioniert der Portionen-Umrechner automatisch.
ingredients:
  - "500g Hauptzutat"
  - "2 EL weitere Zutat"
  - "Salz und Pfeffer nach Geschmack"

# ── Zubereitung ──────────────────────────────────────────
instructions:
  - "Erster Schritt — klar und in ganzen Sätzen."
  - "Zweiter Schritt."
---

> «Ein persönliches Zitat zum Gericht.» — Dein Name

## Über dieses Rezept

Erzähle die Geschichte hinter deinem Rezept!

## Tipps

- Dein bester Tipp für das Gelingen.

## Variationen

- Eine Abwandlung, die du empfehlen kannst.
```

### Schwierigkeitsstufen

- `Einfach` — Anfängerfreundlich, unter 30 Minuten
- `Mittel` — Etwas Technik erforderlich
- `Schwierig` — Fortgeschritten, erfordert Übung

### Kategorien

Erstelle die Kategorien, die für dein Rezept sinnvoll sind! Einige Beispiele:

- Frühstück, Hauptgericht, Dessert, Suppe, Salat, Vorspeise, Beilage, Snack
- Italienisch, Indisch, Japanisch, Mexikanisch, Französisch, Thai, usw.

## Lokal ausführen

```bash
hugo server -D
```

Dann http://localhost:1313/hugo_test/ im Browser öffnen.

## Build erstellen

```bash
hugo -d docs
```

Die statische Website wird im Verzeichnis `docs/` generiert (für GitHub Pages).

## Projektstruktur

```
content/
  recipes/            # Alle Rezept-.md-Dateien kommen hier rein
static/
  images/recipes/     # Rezeptbilder (Querformat, ca. 8:5)
layouts/
  home.html           # Startseite (Hero, Rezept der Stunde, Raster)
  recipes/            # Rezeptliste & Detailseite
  taxonomy.html       # Kategorien-/Schlagwort-/Mitwirkenden-Übersichten
  term.html           # Einzelne Kategorie/Schlagwort/Mitwirkende(r)
  partials/           # Rezeptkarte, Fonts, Theme-Overrides
assets/
  css/cookbook.css    # Das komplette Design-System
archetypes/
  recipes.md          # Vorlage für `hugo new content/recipes/…`
themes/
  PaperMod/           # Hugo-Theme (Git-Submodul)
```
