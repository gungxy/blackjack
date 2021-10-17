# BLACKJACK DESIGN SPECIFICATIONS

It is not the finalized version, and it's in progress. Please visit later. 

## Team Members

Peng Huang phuang@bu.edu U50250882

Ze Yu zey@bu.edu U32088225

Hong Xin hxin@bu.edu U05528604



## Instructions

Simply compile and run the Main, nothing special to note. 

Welcome to contact [phuang@bu.edu](mailto:phuang@bu.edu) if you encounter any issues with compilation and execution.



## Class Descriptions

In development, the classes are organized as a well-designed structure with packages as follows. 

![structure](structure-1.png)



Main class: The entrance of the program of games. 

Utility class: It contains a few utility fields, such as ANSI colors used in the terminal output, and methods, such as prompting user, getting input integer from the user, and random integer generation.

PokerCard class: A poker card with rank, suit, and orientation. 

PokerCardGame class: A game played with poker cards. 

PokerCardPlayer class: A player playing with poker cards. 

PokerCardGameUtiltiy class: It contains utility methods for poker card games, such as gernerating a standard deck of 52 poker cards in random order. In the future, it could be added more utility methods related with poker cards. 

PokerCardSuit enum: It stands for one of the four suits of poker card, including spades, hearts, clubs, and diamonds.

Action enum: It stands for the action of BlackJack-like game, like Hit, Stand, Split, and Double Up. It's used as a medium for messages delivery between the games and players. 

BlackJackLikeGame class: It contains all the common features and methods shared by BlackJack game and Trianta Ena game, such as dealer, players, start, printing table, getting game result and so on. 

BlackJackLikePlayer class: It contains all the common features and methods shared by BlackJack game player and Trianta Ena game player, such as receiving a poker card, print all the cards in hand. What's more, it could act as two roles, Dealer, and Ordinary Player, by implementing the Dealer interface and OrdinaryPlayer interface. 

Dealer interface: A role of BlackJack-like player's. It can prepare a deck of poker cards and deal a poker card.

FaceValueCalculable interface: It should be implemented by face value calculators of various BlackJack-like games. It provides uniform motheds protocol, like calculating the total face value of a hand of poker cards, and judging whether the combination of a hand of poker cards is natural. 


GameResult enum: 3 game results: Win, Lose, and Draw. 

OrdinaryPlayer interface: A kind of role of BlackJack-like player. It contains basic capabilities of playing a BlackJack-like game, like receiving a poker card, beting, and so on. 

BlackJackFaceValueCalculator class: It implementes the FaceValueCalculable interface, providing specific calculation based on the rules of BlackJack game, like  calculating the total face value of a hand of poker cards, and judging whether the combination of a hand of poker cards is natural.

BlackJackGame class: It's a BlackJack game, inheriting methods and fields from BlackJackLikeGame. It has exclusive methods like processing split action and double-up action. 

BlackJackPlayer class: It's a player for BlackJack game, inheriting from BlackJackLikePlayer. 

TriantaEnaFaceValueCalculator class: It implementes the FaceValueCalculable interface, providing specific calculation based on the rules of Trianta Ena game, like  calculating the total face value of a hand of poker cards, and judging whether the combination of a hand of poker cards is natural.

TriantaEnaGame class: It's a Trianta Ena game, inheriting methods and fields from BlackJackLikeGame. It has exclusive methods like processing split action and double-up action. 

TriantaEnaPlayer class: It's a player for TriantaEna game, inheriting from BlackJackLikePlayer. 

ChooseDealerStrategy interface: A method protocal for strategy of choosing a dealer. 

ChooseDealerStrategyImplOrder class: A specific implentation of ChooseDealerStrategy interface, based on sort order of players. It's used in TriantaEnaGame. 

ChooseDealerStategyImplRandom class: A specific implentation of ChooseDealerStrategy interface, based on random. It's used by BlackJackGame. 

HitProcessStrategy interface: A method protocal for strategy of processing the hit action. 

HitProcessStrategyImpl class: A specific implentation of HitProcessStrategy interface, it's used by both BlackJackGame and TriantaEnaGame. 

StandProcessStrategy interface: A method protocal for strategy of processing the stand action. 

StandProcessStrategyImpl class: A specific implentation of StandProcessStrategy interface, it's used by both BlackJackGame and TriantaEnaGame. 

DoubleUpProcessStrategy interface: A method protocal for strategy of double-up action. 

DoubleUpProcessStrategyImpl class: A specific implentation of DoubleUpProcessStrategy interface, it's used by both BlackJackGame.





**to be continued**




































