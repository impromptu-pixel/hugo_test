# Our Community Cookbook

A collaborative Hugo-based cookbook where everyone can share their favorite recipes.

## Adding Your Recipe

1. Create a new `.md` file in `content/recipes/` with a URL-friendly filename (e.g., `my-recipe.md`)
2. Use the template below for your front matter
3. Write your recipe content in the body
4. Submit via pull request!

### Recipe Template

```markdown
---
title: "Your Recipe Name"
date: 2026-06-11
draft: false
description: "A short description of the dish"
categories: ["Category"]
tags: ["tag1", "tag2"]
contributors: ["Your Name"]
servings: 4
prep_time: "15 min"
cook_time: "30 min"
ingredients:
  - "1 cup ingredient"
  - "2 tbsp ingredient"
instructions:
  - "Step 1: Do something"
  - "Step 2: Do something else"
difficulty: "Easy"
---

## About This Recipe

Tell the story behind your recipe!
```

### Difficulty Levels

- `Easy` - Beginner-friendly, under 30 minutes
- `Medium` - Some technique required
- `Hard` - Advanced, requires practice

### Available Categories

Create whatever categories make sense for your recipe! Some examples:
- Breakfast, Main Course, Dessert, Soup, Salad, Appetizer, Side Dish, Snack
- Italian, Indian, Japanese, Mexican, French, Thai, etc.

## Running Locally

```bash
hugo server -D
```

Then open http://localhost:1313 in your browser.

## Building

```bash
hugo
```

The static site will be generated in the `public/` directory.

## Project Structure

```
content/
  recipes/          # All recipe .md files go here
layouts/
  recipes/          # Custom recipe templates
  partials/         # Theme overrides
assets/
  css/              # Custom styles
themes/
  PaperMod/         # Hugo theme (git submodule)
```