# Thread question pack: «Πριν από τα λόγια» / "Before the words"

Five plain questions an actor can ask about a scene before learning the lines,
in Greek and English. Each has a short hint and the name of the idea in two
term registers.

The pack is written for **Aristophanes**, a rehearsal app for actors, where
the questions sit in a feature called Thread. It is published here as open
content so that anyone can read it, translate it or reuse it.

It holds questions only. It contains no text from any play.

## The questions

| id | English | Greek | Shown in the app |
|---|---|---|---|
| `scene.before` | What happened just before? | Τι έγινε λίγο πριν; | yes |
| `scene.where` | Where am I, and when? | Πού είμαι, και πότε; | yes |
| `scene.want` | What do I want from them in this scene? | Τι θέλω από αυτούς σε αυτή τη σκηνή; | yes |
| `scene.obstacle` | What's in my way? | Τι μου στέκεται εμπόδιο; | yes |
| `scene.event` | What is the event of the scene? | Ποιο είναι το γεγονός της σκηνής; | not yet |

The hints, and the term each question goes by in each register, are in the
JSON files.

## Files

- [`thread.en.json`](thread.en.json): English pack, version 1
- [`thread.el.json`](thread.el.json): Greek pack, version 1
- [`LICENSE`](LICENSE): the Creative Commons Attribution-ShareAlike 4.0 International legal code

## Format

Each file is one pack.

Pack level:

| field | meaning |
|---|---|
| `id`, `version` | the pack's name and its version number |
| `language` | `el` or `en` |
| `title` | the pack's title in its own language |
| `licence` | `CC BY-SA 4.0` |
| `attribution` | the credit line to reuse (see below) |
| `termRegister` | which set of terms the labels use: `knebel` (the app's default, for example «προτεινόμενες συνθήκες») or `older` (for example «δοσμένες συνθήκες») |
| `fundedBy` | reserved for a funding source; `null` in version 1 |
| `prompts` | the questions |

Per prompt:

| field | meaning |
|---|---|
| `id` | stable id, for example `scene.want` |
| `text` | the question |
| `hint` | one line of help under the question |
| `tradition` | where the question comes from: `stanislavski`, `knebel` or `hagen` |
| `terms` | the name of the idea in each register: `{"knebel": …, "older": …}` |
| `shareable` | a flag the Aristophanes app reads; `true` for every prompt in version 1 |
| `render` | `false` means the question is in the pack but the app does not show it yet; absent means shown |

An app that uses the pack should key any saved answer by prompt `id` and pack
`version`, so the pack can grow without breaking what people have written.

## Licence and credit

[Creative Commons Attribution-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/)
(CC BY-SA 4.0). You may copy, adapt, translate and redistribute the pack,
including commercially, if you:

1. **credit it** with the `attribution` line from the file you used,
   and say if you changed anything, and
2. **share what you make from it under the same licence.**

The `attribution` lines read:

- English: Aristophanes · "Before the words" (Thread). Questions from the Stanislavski–Knebel tradition and Uta Hagen's questions.
- Greek: Aristophanes · «Πριν από τα λόγια» (Thread). Ερωτήσεις από την παράδοση Στανισλάφσκι–Κνέμπελ και τις ερωτήσεις της Ούτα Χάγκεν.

## Where the questions come from

The questions follow the Stanislavski and Knebel tradition of scene analysis,
and Uta Hagen's questions (the one about what is in the way is hers). Each
prompt's `tradition` field says which. The wording is plain language written
for this pack.

## Translations

A translation is an adaptation, so it is also CC BY-SA 4.0. Keep the ids and
the structure and change the texts, the hints, `language` and `title`.
