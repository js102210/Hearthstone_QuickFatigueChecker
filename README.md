# Hearthstone_QuickFatigueChecker
Command-line program to calculate Fatigue advantage in Hearthstone given both players' current life totals, draw pile numbers and hero powers available.

Note: this project is currently deployed and usable at the following URL:
https://quickfatiguechecker.glitch.me/?fbclid=IwAR0R1khcmB3okkwFupzugbNDTLxTlaViunWgAnvvfirEPPIk7zNyRL-R61M

You can still view and download the source code if you would like, but if you just want to use the tracker, it will probably be more convenient to use the link above.

This app is a calculator to be used while playing Hearthstone to calculate which player is "ahead" in fatigue. To use, simply read the instructions printed to the console and provide requested inputs.

WHAT IT DOES:

Given the relevant info, the calculator finds out how many times each player can draw cards before dying to fatigue damage (assuming that's the only damage taken). Whoever can draw more cards before this point is considered "ahead," though both players' "draws to die" values are printed to the console. Calculations assume that hero powers will be used every turn (when advantageous).

For first-time users, you can press enter at the first prompt to receive full instructions and provide requested information one piece at a time.
Familiar users may wish to save time by providing all of the requested information at once, which can be done at the first prompt instead of pressing enter. 

Note when providing the class name, that inputs are case insensitive and ignore extra spaces (Warrior, WARRIOR, and warrior all work, and demonhunter works the same as Demon Hunter).

FOR THOSE UNFAMILIAR WITH HEARTHSTONE WHO ARE INTERESTED IN HOW THE PROGRAM WORKS:
  -In Hearthstone, a player 'dies' when they run out of hp.
  -When a player is out of cards and would draw a card, they lose 1 hp. Each time this happens, the amount of hp lost to the next 'draw' increases by one.
  -Players sometimes have access to a hero power that either gives them additional hp each turn or takes hp away from the opponent.
  - Often, which player is 'ahead' in this situation is obvious, but sometimes one player will have around 40 hp, and the other will have 20, but the second player has 5 more cards in their draw pile, making the calculation confusing to try to do in your head.

How it calculates: 
-Both players' hp values are provided, then reduced by their current fatigue damage. 
-Then, if the player is still alive, they apply their hero power, increasing their own hp or reducing the opponent's. 
-Whichever player can survive more draws this way is printed as the player 'ahead.' Both players' 'draws to die' values are printed. 
