# Word Catalog

A single-file, self-contained web app for building a personal vocabulary and practicing it with spaced repetition — plus an AI-generated reading module to pull new words from real context.

## Features

**Dictionary**
- Add words with translation, category, example sentence, and personal notes
- Custom categories with color coding
- Leitner-style spaced repetition (5 boxes, review intervals of 0/1/2/4/7/14 days)
- AI-assisted translation when adding a word (via Claude)

**Study modes**
- Flash cards (flip and self-report recall)
- Multiple-choice quiz
- Type-the-translation drill
- Free practice by category, plus a due-for-review queue

**Stats**
- Totals, mastered count, due-for-review count
- Per-category progress breakdown

**Texts**
- Generates short B1-level English reading texts on a chosen topic (daily life, work & tech, travel & culture, mixed), naturally packed with phrasal verbs and idioms
- Each text comes with a vocabulary breakdown and comprehension questions
- Select any word or phrase in the text to add it straight to the dictionary with context
- AI feedback on your written answers to the comprehension questions

## Tech

Plain HTML/CSS/JavaScript, no build step and no framework — a hand-rolled render-on-state-change loop. Text generation, translation, and answer feedback call the Claude API directly from the client. Data (words, categories, texts) is persisted through a `window.storage` key-value interface, so the app is meant to run inside a host environment that provides that API (e.g. a sandboxed artifact runtime) rather than as a plain static page.

## Usage

Open `word-catalog.html` in a compatible host environment. There is no build or install step.
