# A more thorough guide
This document is intended to explain most of our convention in some detail, giving examples and use cases for most moves. For a quick reference, see the [Full_Reference](../master/Full_Reference.md) document.

You can do three things in Hanab(i):  
 * Play a card
 * Discard a card
 * Give a clue


The point of this (a?) convention is to assign extra meaning to each of these actions to convey more information and ultimately make the game easier.
To start with, I'll give some players' names, so that we can talk about *people* rather than just the cards. Hopefully this makes everything feel a bit more human, but who knows.
Our five players will be:
 * Alice
 * Bob
 * Charlie
 * Dave
 * Eve
# Play and Save clues
Now for a question; what should you think when you receive a clue?

To answer this, I'll start by stating what you _should_ think, assuming that nothing \*special\* is going on and then later I'll define what I mean by something \*special\*. So, assuming nothing else, what should you think when you receive a clue? __It means that the newest newly clued card is playable after all of the other 'relevant' cards have been played__. For now, a 'relevant' card is a clued card in someone's hand that your card could rely on.

1. E.g. Nothing is played on the stacks, Alice has R1, R2, B4, P5, P2 and she is clued red, touching cards 1 and 2. No other cards have been clued. Alice now knows that her first and second cards are red, and that her first card should be playable after any relevant cards have been played. She looks around and sees that there are no other clued cards, so her first card is playable right now and is a Red 1.
2. E.g. The stacks are Y1,B2 and Bob has R3, P4, R2, Y3, R4, meanwhile Charlie has a R1 that has been clued as a 1. Bob is clued 2, touching the Red 2. Bob looks around for any relevant cards and sees that Charlie has a R1. He also looks at the stacks and sees the Y1. Bob concludes that his one is either Yellow or Red, and so he can play it after Charlie plays her R1.

A quick note: We make two rather bold assumptions, which are that as players we don't make mistakes and that we are all perfect logicians. This means that everyone always does the right thing, and if someone doesn't then it's for a good reason. I'm saying this now because it applies to what Charlie should do in example 2 above. Charlie can see the colour of Bob's Red Two and can see that it isn't playable, so she needs to fill in with her unknown one to ensure that Bob's two is playable, so she does. If however, she could see that Bob's two was yellow, then she doesn't need to play her unknown one and everything will be fine, so she can do something else that turn (like give a clue).
If this is confusing at the moment, that's fine, but do be warned that this is the kind of thinking that this convention is geared towards.

Okay, so we can get a player to play their left most unclued card by cluing it, but what should that player think about the other clued cards in their hand? Generally speaking, we give one promise to that player: __The other cards touched by the clue are playable in the future__. This is called the "Good touch principle" and is very helpful. It means that the clued cards in someone's hand will be useful at some point, so that person probably shouldn't discard them. It can also lead to someone playing a card that has been in their hand for a while because "the future is now".

1. E.g. The stacks are R1, Y3, G5, B3, P2 and Dave has a single clued card in his hand, which he knows is a 2. Dave knows that he has been promissed that his 2 will be playable in the future, which means it must be Red. Dave is allowed to play his 2 and a Red 2.

"Let's get a game started then. What should I be thinking when I'm playing?"
Generally you want to do the following:
* Play a playable card if you can, but if you can't then
* Give a good clue (what classifies as good will be defined in more detail later)
* Discard a card
But I hear you ask "but which card should I discard?". This is a good question. I think it's very helpful to know which card to discard, so I'll make some definitions and state some rules to follow.

We define a player's "chop card" as the card that is next in line to be discarded. Without any other thinking, this should be a player's right most card (the card closest to the discard pile). When a player needs to discard, they should discard their chop card, as this way everyone can predict what will happen.

There's just one more thing that I need to say before we start playing, which is about *Save Clues*.
We define a *Critical card* to be a card which only has one copy remaining in play.
E.g. a B5, or a R3 after the other R3 has been discarded.
If you receive a clue that touches your chop card, and it is possible that this clue could be talking about a critical card on your chop, then you are not to interpret this as a playable card, instead you must assume that a card is being saved and can assume almost nothing more. The only promise you are given is that your chop card will be playable in the future. You aren't even promissed that your chop card is the card that you think it is (unless it should be playable, in which case you can play it as long as your first card hasn't been clued - see example 2 / 3)
1. E.g. Eve has R3, R4, B1, Y2, R5 all unclued in her hand and the other R3 has been discarded. She receives a Reds clue, touching cards 1, 2 and 5. Eve looks at the discard pile and sees that the Red 3 is in there, so this could be a Red 3 save clue, and she can't play any of these cards.
2. E.g. The stacks are R2 Y1 G3 B5 P2 and Alice has B1 B3 P1 R4 R3. Alice's hand is unclued. Alice receives a red clue touching cards 4 and 5. Because the card on her chop (position 5) has been touched, Alice looks in the discard pile to see if there are any Red cards that need saving and sees the Red 3. However, Alice then looks at the stacks and sees that a R3 ought to be playable right away, so she is allowed to play her chop card (card 5) assuming it is a Red 3.
3. E.g. Imagine the same setup as example two, but Alice's hand is now R3 B1 B3 P1 R4 R5. Alice again receives a Red clue, and again she looks in the discard pile and sees the Red 3 there. In this case, Alice can't assume anything about her hand (because it sort of looks like a play clue on her front card, but should also be a save) so she assumes it's a save and the only thing she concludes is that her chop card is playable in the future.

A 5's clue on the chop card should always be considered a save clue.
For the sake of using compatible words to [Hypen-ated's convention](https://github.com/Zamiell/hanabi-conventions), I will call this (example 2) "Conditional Chop Focus", although I wouldn't focus too hard on this name.

The next two things I want to cover are Chop Moves and Finessing, both of which are useful but they are certainly not equally fun.

# Chop Moves
Sometimes you would prefer it if a player did not discard their chop card. Ofter you can arange this by giving a save clue, but sometimes you don't want to / can't do this either. It it for times like these that we define __Chop Moves__. These are \*special moves\* that have the effect of moving a player's chop a certain number of cards (generally one) forward. There are two kinds of basic chop move: The **Known trash chop move** and the **5's chop move**.
The **known trash chop move** is the more obvious. It states that if you give a clue that touches known trash (e.g. a Ones clue when all of the ones have been played, or a yellow clue when the yellow stack is complete) then all of the cards behind the back most chop moved card are \*important\* and should not be discarded. This results in that player's chop moving forward to accomodate these new \*important\* cards. These \*important\* cards are said to have been "chop moved".

The **5's chop move** only makes sense if you think about it for a bit, but after doing so you will probably come to the correct conclusion. The 5's chop move happens when you clue a 5 in a player's hand and that 5 is one away from their chop. If they had a useless card in their chop position, then you would probably wait to clue the 5, so we state that in this case the chop card has been chop moved, and the 5 had just been saved. If more than one 5 is clued, then as long as the back 5 is one away from chop it is still a 5's chop move.

Some examples:
1. Nothing has yet been played on the stacks and Bob has G4 B3 R5 Y5 R3, with the Red 3 in the discard pile. Bob is clued 5, touching cards 3 and 4. This touches a 5 on his one-away-from-chop, so Bob concludes that this is a 5's chop and marks his fifth card as \*important\* and he won't discard it. If Bob chooses to discard on his turn, he will now discard his second card (the Blue 3).
2. The stacks are R5 Y3 G2 B5 P4 and Charlie has G5 Y1 B1 R2 G4, with the other Green 4 in the discard pile. Charlie receives a Reds clue, touching her fourth card. All of the reds have been played, so this is clearly a known trash chop move and her chop position card (card 5) is \*important\* and shouldn't be discarded. If she needs to discard, she will discard card 4 (because she knows it's trash), and then the B1 (which would then be in position 4) after that.
3. Consider the same set up as above. Charlie could also be clued 2, as all of the 2's have been played and so this is also a known trash chop move with the same effect as in example 2. It might be helpful to note that a 1's clue would be misleading here. If Charlie is clued 1, this clue will touch cards 2 and 3, so she will mark cards 4 and 5 as being chop moved. This saves the Green 4, but also suggests that card 4 (the Red 2) is important for later, which is not true.
 
# Finessing (Fill in situation)
This is quite a large topic, as this is a key way to get more cards played than would otherwise be possible. It relies on the following observation: People add new cards to the front of their hand, so this is where you are most likely to find playable unclued cards.
We all know that we don't make mistakes, so what should you think in the following situation:
1. The stacks are R2 Y1 G4 B4 P1
2. Charlie has B1 R4 Y2 G2 B3
3. Alice clues Red to Charlie, touching card 2
4. You have no clued cards
5. Your turn is immediately before Charlie's

It is clear that Alice has given Charlie a "bad" clue, as Charlie will conclude that her red should be a playable Red 3, but it is in fact a Red 4 and so it won't be playable on her turn. However, Alice is a perfect logician and would never give a truely bad clue, so this must have some greater meaning. We define the situation to be a **"Fill in" situation**, where someone _**thinks**_ they have a playable card that needs to be played first before the card that has been clued.

"So who should play and which card should they play?"

I'll get to that in a minute, but first I want to get some motivation / justification out of the way. If a player has lots of clued cards in their hand that aren't playable at the moment, then their hand is effectively smaller until they can play those cards. This means that there are fewer unclued cards on the table to clue and genereally work with, which is a bit sad. Therefore, we would like to be able to tell players with clued cards to play those cards in order to free up their hands. With that being said, here is how to play through a Fill in situation:
1. Is it someone else's responsibility? If it is then I can just let them play the card and everything should be fine.
2. I can see that no one else is going to fill in, so I need to play something, which card should I play?
* Do I have any relevant clued cards? (Do not inclued chop moved cards here, as they have not been clued!) If I do, I should play the left / front most such card.
* If I don't then I should play my front most unclued card.

We call option 3 a **prompt**, and option 4 a **finesse**, for consistency with [Hypen-ated's convention](https://github.com/Zamiell/hanabi-conventions).
Sometimes, there might be more than one fill in situation at a time. It might even be that a given player is being finessed more than once. In this case, when that player receives the second finesse, they should mark their _second_ unclued card as playable, because their first unclued card is already accounted for. 












