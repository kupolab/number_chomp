# Number Chomp!

A modern browser-based recreation of the classic educational game **Number Munchers** (MECC, 1986). Built with vanilla HTML, CSS, and JavaScript in a single self-contained file.

## How to Play

Open `index.html` in any modern browser. No build tools, servers, or dependencies required.

### Controls

| Key | Action |
|-----|--------|
| Arrow Keys | Move Chompy around the grid |
| Spacebar | Eat the number on the current tile |
| Escape / Tab | Pause / Resume |
| Enter | Confirm (menus) |

### Goal

Each round displays a **rule** at the top of the screen (e.g. "Multiples of 4"). Your job is to move Chompy around the grid and eat **only** the numbers that match the rule.

- **Correct number** &rarr; score points and clear the tile
- **Wrong number** &rarr; lose a life
- **Eat all correct numbers** on the board to advance to the next level

### Scoring

- +100 points per correct number
- **Combo multiplier**: consecutive correct answers multiply points (x1, x2, x3...)
- Combo resets on a wrong answer or death

### Lives & Continues

- You start with **5 lives**
- Lose a life by eating a wrong number or being caught by a Grumblin
- At **0 lives**, the game is over
- You get **3 continues** to retry from the same level (press Space on the Game Over screen)
- After all continues are used, you must restart from Level 1

### Enemies: Grumblins

Grumblins roam the grid. If one lands on the same tile as Chompy, you lose a life and respawn at the center. They get faster and more numerous as you level up.

## Game Modes

1. **Multiples** &mdash; eat numbers that are multiples of X (e.g. "Multiples of 4")
2. **Factors** &mdash; eat numbers that are factors of X (e.g. "Factors of 36")
3. **Primes** &mdash; eat all prime numbers
4. **Equals** &mdash; eat numbers equal to an expression (e.g. "3 + 5 = ?")
5. **Inequalities** &mdash; eat numbers satisfying a condition (e.g. "> 12")

## Level Progression

- **Level 1**: small number range (1-40), 2 slow Grumblins, easy rules
- Each level: number range expands, Grumblins speed up slightly, a new Grumblin is added every 2 levels (max 6)
- The rule difficulty increases every few levels (e.g. Multiples of 2 &rarr; Multiples of 7)

## Tech

- Single `index.html` file &mdash; no build tools, no frameworks
- Canvas-based rendering at 60fps
- Web Audio API synthesized sound effects (no audio files)
- Google Fonts (Press Start 2P) for the retro pixel aesthetic
- Responsive to viewport size
