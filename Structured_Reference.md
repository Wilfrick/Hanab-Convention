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
For the sake of using compatible words to [Hyphen-ated's convention](https://github.com/Zamiell/hanabi-conventions), I will call this (example 2) "Conditional Chop Focus", although I wouldn't focus too hard on this name.

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
   1. Do I have any relevant clued cards? (Do not inclued chop moved cards here, as they have not been clued!) If I do, I should play the left / front most such card.
   2. If I don't then I should play my front most unclued card.

We call option 2.i) a **prompt**, and option 2.ii) a **finesse**, for consistency with [Hyphen-ated's convention](https://github.com/Zamiell/hanabi-conventions).
Sometimes, there might be more than one fill in situation at a time. It might even be that a given player is being finessed more than once. In this case, when that player receives the second finesse, they should mark their _second_ unclued card as playable, because their first unclued card is already accounted for.

[Add examples here]

## Reverse Fill in
Sometimes the card that you are asking to be played from a fill in situation is in a player's hand who plays after the player that you clued, e.g.:
1. The stacks are R3 Y3 G5 B4 P2
2. Dave has G1 G3 R5 B5 P4, with nothing clued
3. Eve has R2 B3 G2 R4 Y5, with the Red 4 clued as red and the Yellow 5 clued as a 5.
4. Charlie clues Red to Dave, touching card 3 as a playable Red.
What should Dave make of this? 

Dave looks around at the other player's clued cards, as well as their front cards. Dave notices that Charlie has a Red 4 that she might try to play to fill in. Dave chooses to wait, not playing his red card. When Charlie plays her Red 4, Dave knows that his Red card was infact the Red 5, and he can now play it.

Here are a few more examples:
1. The stacks are R5 Y1 G5 B4 P2
2. Bob has G1 R1 Y4 P4 B5, where the B5 has been clued as a 5 (5 save) and the Y4 and P4 have been clued as a 4 (a 4 save because the other Y4 is in the discard pile).
3. Charlie has P3 P1 B2 B4 P5, where the B4 is clued as blue but is clearly not useful, and the P5 has been clued as a 5 (5 save).
4. Alice clues Purple to Bob, highlighting the P4 as purple. Bob now knows that this card is a P4, and also that Alice wants it to be played.
5. Bob looks around and sees the Purple 3 in Charlie's first position, so he discards this turn.
6. Charlie sees that the P4 is supposed to be playable, so she fills in. Her blue card is clearly useless, and her 5 won't help (she needs to play the purple 3), so she blind plays her front card.
7. Bob can now play the P4 on his next turn.

Sometimes, multiple players might have the same playable card in position 1. In this case, the last player with that playable card should be the one to play it:
1. The stacks are R1 Y3 G1 B1 P2
2. Alice has B2 G4 P5 P1, all unclued
3. Bob has B2 G1 R2 Y5, with the Y5 clued as a 5 (5 save)
4. Charlie has G4 B5 B3 Y4, all unclued
5. Eve clues Charlie 3, touching card 3.
6. On Alice's turn, she sees that someone else (Bob) could be the one to fill in, so she doesn't play.
7. Bob might be a bit confused because he expected Alice to play her blue 2, but she didn't. Bob concludes that she didn't play because she could see someone else with the blue 2, so he has it. Bob plays his front card.

(This probably needs some more examples)

# Reducing ambiguity
It's time to address a slightly sad topic. I know I said that we assume every player is a perfect logician and that we don't make mistakes, but in reality sometimes you do, or sometimes you just can't see how to get out of a sticky situation without making a "mistake" or giving a clue that you know might result in two people ending up with the same clued card in their hands.
When someone figures out that they have the same card in their hand as someone else, they have a few options:
1. They could do nothing. Sometimes you don't need to do anything, just let the other player do what they want and everything will work out okay.
2. You can discard your known duplicate. This is called a __"Sarcastic Discard"__ and it tells another player that they have this card at the front of their relevant clued cards.

# Fix Clues
It gets more interesting if the players don't even know that a bad card has been duplicated. In this case, sometimes the other team members need to use a clue to fix the situation. Using a clue in this way is a bit sad because it feels like a waste of a clue, so we agree that you would never give a "bad" fix clue. That is, if more than two clues are needed to fix a certain situation then we agree just to let it play out.

(Should probably be reworded)

# More advanced plays
If you understand how filling in works, then you are probably ready to start on some more advanced moves.

With the convention as stated above, most teams will have a good chance of winning a given deck. Sometimes it won't be possible, but often the team will get pretty close. How can we ensure that more of those close games become full score wins?
If you've got this far in the document then you probably will agree with the statment that, most of the time, having more clues available as a team makes the game easier. So how can we make more clues available? We can either generate more clues, or use fewer clues. Discarding more just brings the end of the game round earlier, so that's not a great solution. We are left with trying to find ways to use fewer clues.

# The Play Baton
Sometimes a player has a known playable card in their hand and someone else has just picked up a playable card. Wouldn't it be nice if the player with the known playable card could somehow tell that other player that they have a playable card?
E.g.
1. The stacks are R3 Y2 G3 B3 P5 
2. Alice has R4 G2 B1 B2, all unclued
3. Bob has G4 P3 P2 Y1, all unclued
4. Charlie has B2 P2 B4 G5, with the G5 clued (5 save) and the B4 clued (Blue play clue)
5. Dave has Y1 Y2 Y3 R3, all unclued
6. Dave clues Red to Alice, touching card 1
7. Alice considers if she needs to wait for a reverse fill in, but sees that she doesn't need to because no one has the R4 either clued in their hand or on their finesse position.
8. Alice notices that Bob has a playable card in his hand in his finesse position.

The question now becomes: How can Alice tell Bob that he has a playable card without using a clue?
We need to agree on some structure to help us here, so we agree on the following:
If Alice chooses not to play, and there is no good reason to do so (if she had to give a save clue then this doesn't apply), then she is stating that she can see at least one card on _someone's_ finesse position that is playable right now.
Who has this playable card? And for that matter how many cards can she really see?
All that the other players know is that at least one of their combined finesse position cards are playable. Now if a certain player can't see any playable cards in anyone else's finesse positions clearly they have the playable card. In the example above, Alice doesn't play. Bob will conclude that he has a playable card in position 1 because he can't see any other playable cards in Charlie's or Dave's finesse positions. What can Charlie and Dave conclude? To answer that we will need to add some more structure, but it might help to think it through with an example:

1. The stacks are R3 Y2 G3 B3 P5 
2. Alice has R4 G2 B1 B2, all unclued
3. Bob has G4 P3 P2 Y1, all unclued
4. Charlie has B4 P2 B4 G5, with the G5 clued (5 save) and the B4 clued (Blue play clue)
5. Dave has Y1 Y2 Y3 R3, all unclued
6. Dave clues Red to Alice, touching card 1
7. Alice considers if she needs to wait for a reverse fill in, but sees that she doesn't need to because no one has the R4 either clued in their hand or on their finesse position.
8. Alice notices that Bob has a playable card in his hand in his finesse position.

Note that this is exactly the same as before, except that now Charlie also has a playable card on slot 1. What will happen?
1. Alice refuses to play her known playable R4. This tells everyone that Alice can see at least one playable card in someone's finesse position.
2. Bob thinks that this is talking about Charlie's finesse position, so he discards.
3. Charlie is confused because she thinks Bob should have played. She thinks about it and realises that when Bob didn't play he was effectively also saying that he could see at least one playable card in someone's finesse position. She looks around and concludes that she must have a playable card in slot one.
4. Should she play this card?

Well, she could. If she does, then Bob will think that everything is normal, Alice can play, and everything seems fine. There is just one slight issue though. Bob's playable Green 4 is no longer on his finesse position, and therefore can't be targeted by the same strategy on the next go round. Wouldn't it be nice if __both__ Bob and Charlie could somehow end up knowing that their finesse position cards are playbable?

What would it mean if Charile didn't play? We define the following: It means she can see at least one playable card in the group of cards that Alice was originally talking about (I'll call this the "track"). Bob can now conclude that he also has a playable card (in what is now slot 2). Dave still doesn't actually know if he has a playable card or not in slot one, but he can see at least one playable card in the group of cards that Alice was originally talking about, so he does't think he has a playable card yet and just discards. Alice is free to play. Now what should Bob do?
To recap, Bob has already not played once, telling everyone else that he can see at least one playable card in the set of cards Alice is talking about. The card that he could see was the playable B4 in Charile's hand.
Charlie then didn't play, telling everyone that she can see at least one playable card in the set of cards that Alice was talking about. She is talking about the G4 in Bob's hand.
Bob can now conclude that he has a playable card in (what is now) slot 2. If he doesn't play, he would be stating that he can see __another__ playable card in the group of cards Alice was talking about __in addition to__ the playable B4 in Charlie's hand. But he doesn't want to say this, so he plays his playable G4.
This tells everyone that Bob could see exactly one playable card in the set of cards that Alice was talking about, so now Dave knows that his (now second) card is in fact not playable at the moment.

We are almost there! There is just one more situation that I want to consider before setting everything out formally. Consider the following setup: 
1. The stacks are R3 Y2 G3 B3 P5 
2. Alice has R4 G2 B1 B2, all unclued
3. Bob has G4 P3 P2 Y1, all unclued
4. Charlie has B2 P2 B4 G5, with the G5 clued (5 save) and the B4 clued (Blue play clue)
5. Dave has Y1 Y2 Y3 R3, all unclued
6. Dave clues Red to Alice, touching card 1

7. Alice chooses not to play, so she discards the B2 and picks up the Y3.
8. Alice's hand is now Y3 R4 G2 B1, with the R4 clued as playable
9. Bob knows that Alice discarded to tell someone that they had a playable card, and he is the target of this move.
10. Bob looks at Alice's hand and notices the Y3 in positon 1.
11. Bob would very much like to get Alice to play the Y3 without having to 'waste' a clue on it, so how can he do this?

We agree that Bob is allowed to consider Alice's finesse positon when thinking about whether he wants to play or pass on this 'playable' card

12. Bob doesn't play, telling the group that he can see at least one person with a playable card in their finesse position.
13. Charlie discards because she can see the playable card in Alice's finesse position
14. Dave discards for the same reason
15. Alice might now be confused because she thinks that Bob should have played. She thinks about it and concludes that Bob didn't play because she has picked up a new playable card in slot one.
16. Alice plays this card to demonstrate that she can only see one other playable card in the original finesse positions.
17. Everyone now knows what's going on.


We are now ready to turn this into a format definiton, but first it might be useful to have a word for the set of cards that Alice is talking about, so let's give a definiton for that first:
We define a __track__ to be a subset of the cards in each players' hands. A __track__ talks about the specific card in a player's hand, rather than the position in their hand. So if your first card is part of a track, and you discard, now your second card is the card in the track.
We can now give the full definition for the play baton.
We define the __Play Baton__ as follows:
I will call the player that chooses to start a play baton to be the initiator.
Playing your track card __kills the baton__.
Doing something really important *that you __had__* to do __drops the baton__. (Things like giving save clues and chop moves)
Doing almost anything else __passes the baton__.
When the initiator starts a play baton, the following happens:
1. A new track is created, comprising of the initiator's finesse positon, and then generally everyone else's finesse positon as well (although sometimes it could be everyone else's second finesse positon, or even third)
2. Each player should count up how many playable cards they can see on the track.
3. Each player should __pass the baton__ once for each playable card they can see on the track
4. If the baton is passed to you and you have already passed it once for each playable card, then you should __kill the baton__.
5. If someone __drops the baton__, then you should pause your thought process and wait for it to be their turn again, at which time they __pick up the baton__ and everything can continue as normal.

Please note that what I've written here is a structured way to come to a correct conclusion based on the idea that _passing the baton tells other players that you can see at least one more playable card in the track_. Note also that often some players will be able to figure out what is going on before everyone else, and even though they now know what is going on they may still need to follow the system to make sure that everyone eventually arrives at the same conclusion. If you can guarantee that everyone will come to the correct conclusion then you don't have to follow the step by step process laid out above, but if you aren't sure then I suggest you follow it.

Make sure to think about whether a player not playing is because of a reverse finesse or a play baton. Usually it should be fine, but in the case where it _is_ a reverse finesse, the finessed player __must__ play to avoid any mistakes happening, even if they would rather not because they want to pass what they think is a play baton (unless of course everyone will come to the correct conclusion). In this case, there is no play baton and the reverse finessed player is just making a mistake. 

## Generalised Play Baton
The idea of a play baton can be generalised by changing which cards are included in the track. Each player always only has one card on the track, but it doesn't have to be everyone's finesse positon. It could be that you would like to target someone's second finesse positon (usually the second unclued card), in which case it would be nice to use a play baton with a track that includes this card. For situations like this, we define the concept of a __First/Second/Third/Fourth/Fifth Generalised Play Baton__ as follows:
This acts as a regular play baton, but the track is composed of the initiator's first finesse positon, along with everyone else's First/Second/Third/Fourth/Fifth finesse position.

This will usually only be either a First, Second or Third Generalised Play Baton, because cards that are at the back of people's hands are very unlikely to be playable.
Note that the First Generalised Play Baton is precisely the same thing as a "normal" Play Baton.

If someone doesn't have enough finesse positions (e.g. because they only have 2 unclued cards and someone is trying to give a Third Generalised Play Baton, or if they have 3 unclued cards but the first is already tied up in a separate finesse), then the finesse positon wraps around (so in the first example that player would add their card 1 to the track and in the second example that player would add card 2 to the track.)

## The Early / Late Game
I probably should have introduced the earlygame earlier on in this document, so I'll probably go back and move this section earlier, but for now I'll write it here just so it's recorded somewhere at least.
I will take a moment to discus my understanding of the early game as defined by [Hyphen-ated's convention](https://github.com/Zamiell/hanabi-conventions).
As far as I understand it, they define the early game as the time before the first 'deliberate' discard. This means that everyone can agree on whethere or not the team is still in the early game, or whether they have moved to the mid game. Why do we even bother with a definition like this at all? During the middle of the game, the cards in peoples' hands have a certain structure - (the newly picked up card is the most playable unclued card, the chop card is most likely useless), but at the beginning of the game there is no such structure because the 5 or 4 (or 3) cards that each player was dealt are completely random. Therefore it seems to makes sense to consider a different set of rules when a player doesn't know so much structure about their cards.

~~I think that the key property here is the fact that __the order of the originally dealt cards is random__. __This is a property of those cards__, rather than a global boolean state, so I think a better use of the term "early game" would be in reference to the specific cards that were present from the beginning of the game. 
I will therefore define the concept of an __"Early Game Card"__.
An __Early Game Card__ is a card that has been in someone's hand since the beginning of the game.
If a clue touches any unclued early game cards, then that clue is probably an __Early Game Clue__ and a different set of rules apply.~~

What should those different set of rules be?
At the beginning of the game, the first player must give a clue. Usually they will be able to give someone a play clue, but sometimes they won't. Because most player's finesse position cards won't be playable (and there has been no opportunity to wait to let this change), it doesn't make much sense to allow very unlikely finesses. We therefore agree that any number 5 clues are simply save clues, even if the 5s that are touched aren't on the chop. We call this kind of clue a __5 stall__, which is taken directly from [Hyphen-ated's Convention](https://github.com/Zamiell/hanabi-conventions).

### 2 saves
We would like to be able to make sure that the unclued early game cards are discardable, as this is the state that we will need to assume during the mid game. The most important cards in the game are probably 2s followed closely by 5s. (You can disagree with me here if you want, but I think it's true based on (total score that you would miss out on by not playing any copy of that card)/(number of copies of that card), with some additional score added for the fact that you get a clue back for playing a 5). We therefore agree that 2s are really important, and should probably be saved in the early game. It bears noting that if both copies of a given two are visible then they are slightly less valuable because the team has more opportunity to give clues that get them played.
The upshot of all of this is the following:
A 2s clue on early game cards is a save clue, even if the chop card isn't touched. 


