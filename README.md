Pattern Hunter

A four-player race to the centre where the traps follow a hidden maths rule. Read the clues, crack the pattern, and get there first.

Built for the Syntax Error hackathon at IIT Roorkee.

The idea

Most trap-and-race games are pure luck: you step, you get punished, you try again. Pattern Hunter turns that around. Every game, the computer secretly picks one maths rule that decides which squares are traps. The player who works out the rule from the clues, instead of guessing, gets a real edge.

How a square is described

The board is 13 × 13. Every square has two numbers, shown as a·b:

a is the distance to the nearest top or bottom edge (the edge row counts as 1).
b is the distance to the nearest left or right edge.

The board is mirrored, so the same labels appear in all four corners and every player faces the same puzzle. The four start corners and the gold centre are always safe.

How to play
Press Start game, enter up to four names, and tick CPU for any player you want the computer to control.
Each human answers the same arithmetic question. The fastest solver moves first.
Players take turns, one step at a time (up, down, left or right). Each turn lasts 20 seconds.
The game starts with 2 red squares (known traps) and 2 green squares (known safe). A green number counts the traps on that square's four sides.
A free hint reveals one more square every 60 seconds.
Stepping on a trap bounces you back and you miss your next turn. A second trap in a row sends you back to your corner. Stepping onto an opponent knocks them back one square.
When you think you know the rule, press Declare the rule. Each player gets one guess. A right answer makes you immune to traps for 3 steps and ends all guessing. A wrong answer costs two turns. The game never shows which rule anyone picked.
The first player to reach the gold centre wins.

New to the game? Try Practice mode from the start screen. It uses an easy rule, shows many clues, and has no timers or penalties.

Features
Hidden maths rule picked from a family of 16, different every game
Four players on one screen, with optional computer players that read the green numbers
Arithmetic quiz to decide the move order
20-second turn timer and timed hints
Practice mode with a coaching panel
Player names, win counter, reaction emojis, three board themes and three token shapes
Sound effects for a normal step, a trap and a win (Web Audio, no files needed)
Animated tokens, confetti and a winners' podium
Design decisions
Clues, not luck. Every game starts with few clues, but only if at least four of the 16 rules fit all of them. An early guess faces several plausible rules.
Always winnable. Each rule was checked by computer to leave a safe path from every corner to the centre, and no rule makes the start corners or the centre a trap.
Fair board. The mirrored layout gives all four players the same puzzle.
Who moves first. In simulations of simple computer players on this board, the first player won about 33% of games and the last about 17%, so moving first is an advantage. That is why the fastest quiz solver moves first. These simulations used basic bots, not people, so treat the numbers as a rough guide.
Tech

Plain HTML, CSS and JavaScript in a single file (index.html). No frameworks and no build step. The only outside resource is the Orbitron font from Google Fonts, which falls back to a system font if it can't load.

Run it yourself
Download Pattern Hunter.html
Open it in any modern browser.

To host it free, use GitHub Pages or drag the file onto Netlify Drop.

Inspiration
Zendo and Eleusis: discovering a hidden rule from examples
Minesweeper: numbers that count nearby hidden traps
Mastermind: deducing a secret from feedback
Ludo King: four-player turns, names, reactions and a lively look

The combination is our own: a Zendo-style deduction puzzle turned into a four-player race, where the rule is a maths pattern on the board's coordinates.

Limitations and future work
Play is hot-seat only, on one screen. Online play on four devices is the next step.
Computer players race using the clues but never guess the rule.
Because players share a screen, others should look away during the arithmetic question and when someone declares the rule.
The game logic was tested with scripts, and the interface has been tried on a limited number of devices. Please report any bugs.
AI assistance

This project was built with the help of Claude (Anthropic), an AI assistant. It was used for brainstorming the game design, writing and revising the code, and creating test scripts.
