# Chorus-lapilli
the typical tic-tac-toe but with a twist: after their first 3 moves, players cannot add new pieces. Instead, they must move their existing 3 pieces to win. Any player with a piece that occupies the center must either move that piece out of the center in their next turn, or win. 

How to play:
1. in the first 6 turns, the player should simply click the square they wish to place a piece in, as with regular tic-tac-toe
2. After the first six turns, the player should first click one of their tiles, then click a destination to move their desired piece to their desired location.

NOTE: Pieces that are in the middle must be moved in that player's next turn, so if any non-center piece is clicked in that next turn, the game will ignore it.

Code overview: 
sixpieces():
Sees if the game has gone long enough to have six pieces on the board.
If so, switches handleclick() to chorus mode, 
where pieces must be moved rather than placed, along with other restrictions

validSquare():
Checks if the square has a piece in it. 
If so, return true, as we can move this piece 

validMove(src, i)
Takes the first piece clicked, and the destination click. 
Then checks if the move is valid: if the piece will be moved to an 
adjacent square, and if the square it's being moved to is empty

mustMove()
Checks if the current player has a piece in the center of the board. 
If so, the player must move the piece. Returns true

These above functions are only used when in chorus mode. 

When handleClick(i) is in chorus mode, 
it uses those functions to force players to move pieces, 
rather than place them, 
and also makes sure that the players can only do legal moves. 
The handleclick(i) function also uses those functions to 
determine the game state, and will alter Board variables 
accordingly to determine the game state, 
and use that information to act accordingly. 

