# Zach Gage — On Product

## The Core Product Method

Zach Gage's product philosophy is built around a single repeatable operation: identify the essential fun in an existing game, then redesign everything that prevents players from reaching it. This is not a UX improvement process — it is a first-principles reconstruction of the product experience, starting from the question "what is this game actually for?"

He does not start with a genre he loves. He has made word games (SpellTower) despite initially disliking word games, chess variants (Really Bad Chess) without being a chess enthusiast, and Sudoku (Good Sudoku) having never played Sudoku before. The outsider position is a product tool: it forces him to ask why the game exists, not assume he already knows.

## Really Bad Chess: Randomness as Product Decision

Really Bad Chess (2016) is a useful case study in how Gage thinks about product. The core insight was not "let's add randomness to chess" — it was a specific observation about what makes chess inaccessible: the game's perfect balance and opening theory create an enormous skill gap that makes the first hundred games discouraging for non-experts.

The product question became: what if you removed the balance entirely? The original concept was to pit two players against each other with genuinely random piece sets. But Gage discovered that total randomness was too perverse — a game that seems to have no rules does not feel like a game at all. He spent significant time engineering the right kind of randomness: thousands of board configurations mapped to difficulty ranks, with gradual shifts in piece distribution as players progress through a ranking system.

The result is a product that democratizes chess. The random pieces mean that a non-expert player has a genuine chance against a stronger opponent, and the familiar board and movement rules mean the underlying chess literacy can grow with each game. The product insight: fairness and balance are not the same thing. A fair game is not necessarily a fun game.

## Good Sudoku: Removing the Busywork Layer

Good Sudoku (2020) represents Gage's fullest expression of the "remove the cake" product principle. Sudoku as traditionally implemented requires players to maintain a mental tracking layer — counting which numbers appear in each row, column, and box — before they can even begin to engage with the puzzle's actual depth.

Gage's product decision was to offload that counting to the software. The app only shows numbers that are possible in a given square given the current board state. A solver runs continuously, detecting what the player knows from their answers and notes, and offers the next relevant technique when the player is stuck.

The product result: "Freed from the burden of busywork, Sudoku becomes one of the best search-style games, and with Good Sudoku and a little practice, anyone can learn it." The game reveals that Sudoku is actually a game of beautiful technique structures — which were always there, hidden under the counting layer that most implementations never removed.

## Knotwords: The Algorithm Is the Product

Knotwords (2022), created with Jack Schlesinger, taught Gage a lesson he considers foundational: "I had been under the mistaken impression that the magic of a simple game was in its simple rule set. The magic actually comes from having an amazing algorithmic puzzle constructor."

Gage and Schlesinger spent four of the six development months building the puzzle generator — not the game. The generator had to model player behavior (what steps can a player take, what mistakes will they make, how long will it take them to correct an error) rather than just following rules. The product is not separable from its infrastructure. A puzzle game is only as good as its puzzles, and good puzzles at scale require a generator that understands players.

## Puzzmo: A Platform Product

Puzzmo (2023) extends Gage's product thinking to platform scale. The product insight was drawn from his mother: she tried new games in the newspaper not because she was a gamer, but because games were displayed alongside things she was already reading. The newspaper puzzle page as a product created discovery through adjacency.

Puzzmo attempts to replicate this on the web: a magazine-style layout with multiple daily puzzle widgets, where players can navigate between games and see their own progress memorialized. The platform is explicitly designed to be a community space — "a place where you go and hang out with your friends," borrowing from multiplayer games while remaining a puzzle product. Leaderboards, social groups, and archives are subscription features, but the daily experience is free.

The product philosophy for Puzzmo also includes a permanence commitment: games added to the platform stay permanently rather than rotating out. This is an anti-product-management product decision — conventional platforms rotate content for engagement metrics. Puzzmo's decision reflects a different value: the player's archive and history matter.

## Prototyping Philosophy

Gage prototypes fast and maintains flexibility. For Pile-Up Poker, he "pretended there were rules around placement instead of implementing them with code" in early stages — preserving flexibility to change mechanics without technical debt. He has said: "Sometimes I feel like my best designs are the ones that work right away," a heuristic for identifying strong core concepts. Really Bad Chess required only 10 minutes and a $25 Unity asset to produce a functional prototype. If the core is good, it shows immediately.

He also makes many more things than he releases. By his own account, he makes roughly a hundred prototypes a year and releases approximately one game a year. Most ideas fail; the discipline is in knowing when something has found its essential fun and when it has not.

## Sources

- [How Zach Gage breaks all of the rules in Really Bad Chess — Game Developer](https://www.gamedeveloper.com/design/how-zach-gage-breaks-all-of-the-rules-in-i-really-bad-chess-i-)
- [Knotwords: Gage and Schlesinger at the crossroads — Apple Developer](https://developer.apple.com/news/?id=ti9czxni)
- [Here's how Zach Gage prototyped Puzzmo sensation Pile-up Poker — Game Developer](https://www.gamedeveloper.com/design/here-s-how-zach-gage-prototyped-puzzmo-sensation-pile-up-poker)
- [If you love Wordle and Connections, Puzzmo may be your next daily obsession — Digital Trends](https://www.digitaltrends.com/gaming/puzzmo-announcement-zach-gage-interview/)
- [How Zach Gage is Revolutionizing Classic Games — hey.gg](https://www.hey.gg/blog/zachgage)
