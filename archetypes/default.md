---
title: "{{ replace .File.ContentBaseName "-" " " | title }}"
date: {{ .Date }}
draft: true
description: "A short description of the dish"
categories: ["Uncategorized"]
tags: []
contributors: ["Your Name"]
servings: 4
prep_time: "15 min"
cook_time: "30 min"
ingredients:
  - "1 cup example ingredient"
  - "2 tbsp example ingredient"
instructions:
  - "Step 1: Do something"
  - "Step 2: Do something else"
difficulty: "Easy"
---

## About This Recipe

Write a brief story or introduction about this recipe here.

## Ingredients

{{< recipe_ingredients >}}

## Instructions

{{< recipe_instructions >}}

## Tips

- Add any helpful tips or variations here.

## Notes

Any additional notes about the recipe.