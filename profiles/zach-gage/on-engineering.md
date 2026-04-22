# Zach Gage — On Engineering

## Systems Engineering: Simple Rules, Deep Behaviour

Gage's game design engineering is governed by a principle that applies beyond games: the most durable systems are those where simple, learnable rules produce complex, emergent behaviour. SpellTower's rules are simple — find words on a letter grid. The depth comes from the scoring system, the letter distribution, and the pressure mechanics. The engineering challenge is balancing these parameters so the system feels fair, learnable, and endlessly interesting.

The engineering discipline: before adding a new rule or mechanic, ask whether the existing system can produce the desired behaviour through emergent dynamics. Complex emergent behaviour from simple rules is a more elegant engineering solution than complex rules that produce complex behaviour directly.

## Tutorial Engineering: The System Teaches Itself

Gage's games are designed so that the first session teaches the player how to play without an explicit tutorial. The engineering of this requires that the starting conditions, the failure modes, and the reward signals all communicate the system's rules through experience rather than instruction.

This is harder to engineer than a tutorial screen. It requires playtesting to identify where new players are confused, then engineering changes to the system itself (not just the onboarding) to address the confusion. The goal: a player who has played for 60 seconds understands the game well enough to proceed.

## Ethical Monetisation Engineering

Gage's monetisation engineering is explicitly designed to avoid dark patterns. Puzzmo's subscription model offers a transparent monthly price, no dark-pattern cancellation flows, no loot boxes, no energy systems, no artificial friction. The engineering of this is not trivial: subscription management, trial periods, and renewal handling all require careful implementation to avoid the patterns that many games use to obfuscate costs.

The engineering standard: the monetisation system should be implementable with a single honest sentence describing what the user gets for their money. Any monetisation architecture that requires a multi-paragraph explanation is probably concealing something.

## Mobile Game Performance Engineering

Gage's games are iOS-native, typically built with Swift and SpriteKit or custom rendering. The performance requirement for a word game is different from a drawing app: the rendering does not need 120fps, but the response to user input must feel instantaneous. A word game that takes 100ms to register a tile tap has failed, even if the frame rate is perfect.

The engineering principle: performance requirements vary by interaction type. Define the performance requirement for each interaction type (tap response, animation smoothness, puzzle generation latency) and test against those requirements independently.

## The Redesign as Engineering Research

Gage's approach to game design includes redesigning existing games — taking a familiar game (Solitaire, chess variants, crossword) and identifying the design decisions that have been inherited without question, then re-examining each one. The engineering equivalent is examining a legacy system's architectural decisions to identify which are load-bearing and which are accidental.

The engineering discipline: regularly examine your architectural assumptions. Some assumptions were correct when made and remain correct. Some were correct when made but no longer are. Some were never correct. The only way to find out is to ask.

## Sources
- [Zach Gage — stfj.net](http://stfj.net/)
- [Puzzmo — puzzmo.com](https://www.puzzmo.com/)
- [SpellTower — App Store](https://apps.apple.com/app/spelltower/id476500832)
- [Zach Gage — Twitter/X design and game philosophy posts]
