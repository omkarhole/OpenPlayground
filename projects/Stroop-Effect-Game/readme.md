
# Stroop Effect Game

A small browser game that tests how well you can identify the ink color of a word rather than the word's meaning — a digital take on the classic Stroop test.

- Live demo: open `index.html` in a browser.

## How to Play

- The prompt shows a color name (word) rendered in a colored ink.
- Your goal: click the button whose color matches the *ink* color (not the word text).
- You have a limited time (default 30 seconds) and a maximum number of mistakes (default 3).

## Controls

- Click a colored button to answer.
- The game starts automatically on page load; click "Play again" to restart.

## Game Rules & Behavior

- Score increments by 1 for every correct selection.
- A wrong selection increments the mistakes counter; reaching the maximum ends the game.
- Timer counts down; when it reaches zero the game ends.

## Files

- `index.html` — the full game (HTML, CSS and JS in a single file).
- `readme.md` — this documentation.

## Configuration

You can edit the following constants near the top of the script in `index.html` to change gameplay:

- `GAME_SECONDS` — total seconds per round (default 30).
- `MAX_MISTAKES` — how many mistakes before game over (default 3).

Other behavior like the number of color choices is controlled by the `pickRandomColors(count)` call in the script.

## Accessibility & Notes

- The UI uses large text and high-contrast color swatches; however, people with color-vision deficiencies may find the game difficult.
- Consider enabling additional cues (icons or labels) for improved accessibility.

## License & Credits

This project is part of the OpenPlayground collection. Use and remix under the repository's license (see the repository root for license details).

Created by contributors to OpenPlayground.
