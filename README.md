# Tic-Tac-Toe

# Functionality
This game has two modes, player vs. player, and player vs. AI. Games can be played with a score count. Scoreboard can be wiped.

# Process
I had a tough time deciding what each module would do. I boiled it down to three modules. One for the board, one for the view, and lastly the interaction between the board and view. Having these modules allowed for me to break down my needs down even further into smaller methods.

I created a factory function to be a template for the players that were going to be created, which kept track of the scores and moves.

This project got me comfortable with using closures to hide data and making what's necessary available.

I changed the squares Nodelist into an array so that I could grab the index of each node.
Added a method to the game board to check if the array element's innerText was undefined. (Empty board)

Having the turn switch between player 1 and player 2 took me a bit to figure out. I decided on using reduce in conjunction with filter to determine the mode. With this function I was able to switch between the two even when in a tie condition.
  *Just calling the board mode method will return the function. It needs assignment, and then calling to run!*

The biggest problem I ran into was when the boardgame array was referenced from the resetGameboard method, it would point to a different version of the array and not the one already instantiated. I changed the boardgame array from a sparse array to an empty one and pushed values into it. Switched the winningCondition method to check the square's innerText instead of boardgame array elements positions.

I created an turn based AI that would randomly select an open square by filtering all the available squares and choosing one at random.
