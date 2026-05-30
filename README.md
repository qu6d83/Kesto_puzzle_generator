# Play Kesto

A minimalist, browser-based playable clone of the Kesto sliding block puzzle. It features an infinite random level generator powered by a high-performance bitboard engine, supporting both responsive touch and keyboard controls.

> **Disclaimer:**
> This is an unofficial, fan-made game. All rights to the original game design, mechanics, and the name "Kesto" belong to Hiking studio. If you enjoy this puzzle, please support the original developers by downloading "Kesto" on Google Play.

## Features

* **Infinite Random Levels:** Automatically generates guaranteed-solvable puzzles across four difficulty tiers (Easy, Medium, Hard, Impossible) using a background Breadth-First Search (BFS) validation engine.
* **Native Controls:** Play seamlessly using keyboard arrow keys (or WASD) on desktop, and intuitive swipe gestures on touchscreen devices.
* **High-Performance Engine:** Utilizes 64-bit integers (Bitboards) and bitwise operations to compute sliding mechanics, collisions, and state validations instantly without freezing the browser.
* **Minimalist UI:** A clean, distraction-free interface that tracks your current step count and focuses entirely on the gameplay.
* **Zero Dependencies:** Built entirely with Vanilla HTML, CSS, and JavaScript.

## Usage

1.  Download or clone this repository and open the `index.html` file in any modern web browser.
2.  Select a difficulty level from the dropdown menu and click "Gen" to create a new puzzle. 
3.  Slide the orange blocks to perfectly land on the blue target outlines. Blocks will only stop sliding when they hit the grid boundary, a dark gray obstacle, or another block.
4.  If you get stuck or make a wrong move, click "Reset" to restart the current level from zero steps.

## Technical Details

To accommodate the infinite level generation in a single-threaded JavaScript environment, the game represents the entire 8x8 grid as a 64-bit integer (`BigInt`). Sliding movements are executed via bitwise shift operations, allowing the BFS algorithm to validate hundreds of thousands of potential puzzle configurations in milliseconds to filter out unsolvable or poorly paced levels.

## License & Attribution

The source code for this project is released under the [MIT License](LICENSE) (Note: This does not apply to the original game concept or design).

*This documentation and the core logic optimization were assisted by Google Gemini.*