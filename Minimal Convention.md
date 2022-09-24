# Minimal Convention
As part of my exploration into different conventions I have discovered a need for a simpler convention to start from. I hope to lay out such a minimal convention in this document.

## Aims
Although this convention should be simple, it should be detailed enough that it fully specifies how a game should be played. Often in more human conventions we leave things up to interpretation or feel, but here I want to explore automated testing of different conventions, so I'll need something with enough formallity that a computer can understand it.

 ---
 
### Convention
This is a list of actions to be taken, in order of importance. Once an action is selected no further actions are considered.

1. Play a card that is marked as playable
2. Clue the lowest rank unclued playable card possible - in this case the front most touched card is the card selected, there is no notion of previously clued cards
3. Discard chop card.
4. Clue the rank of the previous player's last card
---

This is a list of rules for how to mark cards with globally consistent flags - things like `being playable' or `being discardable' or `having been chop moved'. In this case we have very few such flags.

#### System Flags
V: <Value> This is the true identity of the card. This can be seen by everyone eccept the current player, is a read only attribute and is the only non global information that the convention can consider using. It
T: <Touched> This is for a card that has been touched by a clue. It carries extra information in the form of which colour / rank it is, but we ignore this here.
I: <Index> This is the index of the card in a given person's hand. The front most card is card 0 and the back most card is card 3 or 4. N.B. I = -1 is also the index of the back most card.
H: <Hand> This is the offset of the hand from the current player. So a card with H=0 is a card in the current player's hand, whereas H=-1 is a card in the previous player's hand and H=1 is a card in the next player's hand.

These flags are called System Flags because they are updated by the system - no interaction is needed from the convention to keep these up to date. These are also the only flags for which this is true. All other flags need corresponding rules to keep them updated.

#### Custom Flags
IP: <Immediately Playable> This is for a card that fits exactly somewhere on the stacks right now. It does not promise which rank or colour, although that may be deducible.
---
This is a list of rules for modifying the flags of all cards in play in the game. These rules are again applied in order 

#### Flag Update Rules
1. if {n:card[0][n] = T and card[0][n] != IP forall n in I} nonempty => card[0][min{n:card[0][n] = T and card[0][n] != IP forall n in I}] += IP
2. forall h in H forall n in I, card[h][n] -= T


## Expectations
I expect that this convention should be able to play a few cards, but will undoubtably discard important cards and will surely never win. In fact, due to random usless cluing I think that most games will be lost through misplays rather than discards.


## Results
After implementing a system to play hanabi for me in Python 3 and then implementing the above convention and testing it in 10000 trial games I have the following score distribution:
[0, 10, 18, 27, 29, 36, 38, 27, 27, 38, 18, 26, 39, 39, 30, 52, 116, 333, 785, 1455, 2167, 2537, 2008, 145, 0, 0]
This has an average of 19.7 with 90% of the games scoring between 16 and 22. This did much better than I thought, but it still can perform badly. I'm slightly saddened to see that the highest score was only 23, but at least this shows that there is merit in further developement, as it is certainly possible to win this variation of Hanabi.

### Next Steps
I think I'll add some more rules manually (like save clues and maybe good touch principle) to see how much of a difference these simple rules make. I'll probably then need to step back and rethink a bit about trying to keep different rules independent of one another, as ideally I'd like to be able to pick and choose ideas freely to craft an ideal convention.




