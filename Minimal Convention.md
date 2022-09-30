# Minimal Convention
As part of my exploration into different conventions I have discovered a need for a simpler convention to start from. I hope to lay out such a minimal convention in this document.

## Aims
Although this convention should be simple, it should be detailed enough that it fully specifies how a game should be played. Often in more human conventions we leave things up to interpretation or feel, but here I want to explore automated testing of different conventions, so I'll need something with enough formallity that a computer can understand it.

 ---
 
# Convention
This is a list of actions to be taken, in order of importance. Once an action is selected no further actions are considered.

1. Play a card that is marked as playable
2. Clue the lowest rank unclued playable card possible - in this case the front most touched card is the card selected, there is no notion of previously clued cards
3. Discard chop card.
4. Clue the rank of the previous player's last card
---

This is a list of rules for how to mark cards with globally consistent flags - things like `being playable' or `being discardable' or `having been chop moved'. In this case we have very few such flags.

### System Flags
-V: (Value) This is the true identity of the card. This can be seen by everyone eccept the current player, is a read only attribute and is the only non global information that the convention can consider using. It
-T: (Touched) This is for a card that has been touched by a clue. It carries extra information in the form of which colour / rank it is, but we ignore this here.
-I: (Index) This is the index of the card in a given person's hand. The front most card is card 0 and the back most card is card 3 or 4. N.B. I = -1 is also the index of the back most card.
-H: (Hand) This is the offset of the hand from the current player. So a card with H=0 is a card in the current player's hand, whereas H=-1 is a card in the previous player's hand and H=1 is a card in the next player's hand.

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

## Save clues
The next step I would like to take is to add save clues to this convention. Currently no games reach maximum score and this could be happening because required cards are being discarded.
I think I'll impement them as follows:

### Save clues explained
We identify critical cards as any card with rank less than or equal to 4 (we will deal with 5s separately) with one copy discarded that is not already saved or marked as immediately playable. A save clue is a clue that touches the card about to be discarded (the chop card) where that chop card could be critical. The chop card is then marked as saved (CM for historical reasons) and is not discarded. When this card is later needed it will be clued with a play clue when possible. To save 5s the clue must be a 5 clue, but is otherwise treated the same (in particular this still saves only one card).
To make this possible we introduce one new custom flag:

CM: <Chop Moved> This card should not be discarded but is otherwise a normal card. It should be playable at some point.

We also introduce some more logic for the convention:

1. If the next player has no playable card and has a critical card on their chop, give a save clue
2. Play a card that is marked as playable
3. Give a save clue (starting from the next player and working round)
4. Give a play clue (starting from the first card of the next player, working through their cards, then repeating with the next player and so on). The front most touched card is the card selected, there is no notion of previously clued cards
5. Discard chop card.
6. Clue the rank of the previous player's last card

Finally, we need to update the flag update rules:

0. if any{card[0][-1] = T and card[0][-1] could be critical} => card[0][-1] + CM() and Forall h in H forall n in I, card[h][n] -= T.
1. if {n:card[0][n] = T and card[0][n] != IP forall n in I} nonempty => card[0][min{n:card[0][n] = T and card[0][n] != IP forall n in I}] += IP
2. forall h in H forall n in I, card[h][n] -= T

## Expectations
These changes might result in a few more low scoring games due to not being able to give play clues, but I think the current reason that some games get particularly bad scores is because there aren't any playable cards at the beginning and random clues are given which result in lives lost. Having another way to use up clues should help to prevent this, so I actually think the number of low score games should stay mostly the same or even decrease. I hope that we should be able to increase the maximum score from 23, as it should be possible to hold onto most 5s and 4s throughout the middle game. By some rough calculations the team usually has at least 40 clues to work with over the course of a game (50+8-[10-16]) = [42-48] and so assuming that all cards take either 1 or 2 clues to get played (either they get played directly or they get saved and then played) we can affort to save at most 15 of the required 25 cards. This is more than half, so I'd hope there will be games were all required cards get saved, giving a reasonable chance of a 25 card win. Just for fun, I'll make a guess as to how much I think the average score will increase by. I think that each game probably discards 2 or 3 critical cards, but by saving these more cards will become critical and this will eat up more clues. I think therefore that adding these save clues will probably only bring the average up by 1 or 2 cards per game. I think the lower 5% of games won't be affected much but that the top 5% should slide up with a small number of 25 point wins and considerably more (around 5 times as many) 24 point games. Many of these predictions aren't particularly substantiated, but I think it will be interesting to see where my intuition is correct and where it is woefully inadequate.

##Results
