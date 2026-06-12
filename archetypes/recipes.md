---
# ── Basis ────────────────────────────────────────────────
title: "{{ replace .File.ContentBaseName "-" " " | title }}"
date: {{ .Date | time.Format "2006-01-02" }}
draft: true
description: "Eine kurze, appetitanregende Beschreibung des Gerichts (1–2 Sätze)."
# Bild nach static/images/recipes/ legen (Querformat, ca. 8:5):
image: "images/recipes/default.svg"

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
  - "Anrichten und geniessen!"
---

> «Ein persönliches Zitat oder ein kurzer Gedanke zum Gericht.» — Dein Name

## Über dieses Rezept

Erzähle die Geschichte hinter deinem Rezept! Woher stammt es, was macht es besonders, wann kochst du es am liebsten?

## Tipps

- Dein bester Tipp für das Gelingen.
- Noch ein Tipp.

## Variationen

- Eine Abwandlung, die du empfehlen kannst.
