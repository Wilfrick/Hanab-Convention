# Minimal Convention
As part of my exploration into different conventions I have discovered a need for a simpler convention to start from. I hope to lay out such a minimal convention in this document.

## Aims
Although this convention should be simple, it should be detailed enough that it fully specifies how a game should be played. Often in more human conventions we leave things up to interpretation or feel, but here I want to explore automated testing of different conventions, so I'll need something with enough formallity that a computer can understand it.

 ---
 
### Convention
This is a list of actions to be taken, in order of importance. Once an action is selected no further actions are considered.

1. Play a card that is marked as playable
2. Clue the lowest rank playable card possible - in this case the front most touched card is the card selected, there is no notion of previously clued cards
3. Discard chop card.
4. If somehow we are at 8 clues then try to clue an unplayable card (e.g. 1 if all 1s have been played, or R if all Reds have been played)
5. Give a random clue
---

This is a list of rules for how to mark cards with globally consistent flags - things like `being playable' or `being discardable' or `having been chop moved'. In this case we have very few such flags.

#### System Flags
T: <Touched> This is for a card that has been touched by a clue. It carries extra information in the form of which colour / rank it is, but we ignore this here.
I: <Index> This is the index of the card in a given person's hand. The front most card is card 0 and the back most card is card 3 or 4. N.B. I = -1 is also the index of the back most card.
H: <Hand> This is the offset of the hand from the current player. So a card with H=0 is a card in the current player's hand, whereas H=-1 is a card in the previous player's hand and H=1 is a card in the next player's hand.

These flags are called System Flags because they are updated by the system - no interaction is needed from the convention to keep these up to date. These are also the only flags for which this is true. All other flags need corresponding rules to keep them updated.

#### Custom Flags
IP: <Immediately Playable> This is for a card that fits exactly somewhere on the stacks right now. It does not promise which rank or colour, although that may be deducible.
---
This is a list of rules for modifying the flags of all cards in play in the game. These rules are again applied in order 

#### Flag Update Rules
1. if min{x:card[0][x] = T} nonempty => card[0][x] += IP
2. forall H forall I card[H][I] -= T
