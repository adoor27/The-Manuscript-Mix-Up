# The Manuscript Mix-Up

## Repository

https://github.com/adoor27/The-Manuscript-Mix-Up.git

## Description

A text-forward point-and-click puzzle game where the player is a librarian's assistant who must return misplaced books to their proper shelves by solving riddle-like clues left behind by the missing head librarian.

## Features

- Clickable library scenes
  - Each area (reading room, archive, rare books room) is a screen drawn with flat-color rectangles, with clickable shelves, desks, and carts detected using `pygame.Rect` and mouse events. A simple scene manager class switches between rooms.
- Book inventory and shelving mechanic
  - Books are shown as colored rectangles with title text on a cart. The player clicks a book to select it, then clicks a shelf slot to place it, and the code checks the placement against the correct answer.
- Riddle clues from the librarian
  - Clues appear on index cards or notes and describe where each book belongs through wordplay (theme, author, color, or alphabetical order). All clues and answers live in a JSON file, so they are easy to write and edit without changing code.
- Feedback and hints
  - A wrong placement shows a short in-world message (the book "doesn't feel right") and a hint button reveals the next clue after a cooldown timer.
- Story through text
  - Margin notes, catalog cards, and book excerpts reveal what happened to the librarian, shown in a custom text box with a typewriter effect and word wrapping written with `pygame.font`.
- Typography-driven visuals and sound
  - Mood comes from font choice, a limited color palette, and simple effects such as fading text and a flickering lamp (alpha and color changes). Ambient audio (page turns, clock ticking, room tone) from royalty-free sources like Freesound plays through `pygame.mixer`.

## Challenges

- Learning how to structure a Pygame project with a game loop, scene/state manager, and event handling.
- Building reusable UI pieces (buttons, text boxes, word wrap) since Pygame has none built in.
- Designing a data-driven system that loads books, shelves, and clues from JSON files.
- Researching riddle and puzzle design so clues are clever but still fair and solvable.
- Learning how to package the game (for example with PyInstaller) so it can run without a Python setup.

## Outcomes

Ideal Outcome:

- A polished 15-minute game with 3-4 library areas, about 12-15 books to shelve, a consistent typographic style, ambient sound, and an ending that reveals the librarian's fate. It is packaged as a downloadable executable and documented in the repository.

Minimal Viable Outcome:

- A single-room game with 5 books, 5 riddle clues, a working click-to-shelve mechanic, and a win screen when all books are correctly placed. It runs from the repository with `python main.py`.

## Milestones

- Week 1
  1. Create the public GitHub repo with a README and `requirements.txt`, set up the Pygame project in VS Code, and write the story outline and list of books and clues.
  2. Build a prototype with a game loop, one placeholder shelf, and clickable books with select-and-place logic.

- Week 2
  1. Implement correct/incorrect feedback and a win state, and load books and clues from a JSON file (Minimal Viable Outcome reached).
  2. Build the text box with word wrap and a typewriter effect, and write the full set of riddle clues.

- Week 3
  1. Add a scene manager and build the second library area with its books and clues.
  2. Add the hint system, the story notes, and basic sound effects and ambient audio.

- Week 4
  1. Add the title screen and ending, then playtest with friends to check the riddles are solvable and fix bugs.
  2. Polish fonts, palette, and audio, and finalize the README (and package the game if time allows).
