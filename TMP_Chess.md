**Problem Statement:** The problem is to design a Chess Game using Object Oriented Principles.
**Asked In:** <mark class="hltr-lightblue">Adobe</mark>, <mark class="hltr-lightgreen">Amazon</mark>, <mark class="hltr-lightred">Microsoft</mark>, etc.

**Solution:**
These type of questions are asked in interviews to Judge the Object-Oriented Design skill of a candidate. So, first of all we should think about the classes.

The main classes will be:
1. **Spot**: A spot represents one block of the 8×8 grid and an optional piece.
2. **Piece**: The basic building block of the system, every piece will be placed on a spot. Piece class is an abstract class. The extended classes (Pawn, King, Queen, Rook, Knight, Bishop) implements the abstracted operations.
3. **Board**: Board is an 8×8 set of boxes containing all active chess pieces.
4. **Player**: Player class represents one of the participants playing the game.
5. **Move**: Represents a game move, containing the starting and ending spot. The Move class will also keep track of the player who made the move.
6. **Game**: This class controls the flow of a game. It keeps track of all the game moves, which player has the current turn, and the final result of the game.

Let’s look at the details. These codes are self-explanatory. You can have a look at the properties/variables and methods of different classes.
$\quad$[[TMP_ChessSpot|Spot: To represent a cell on the chess board]]
$\quad$[[TMP_ChessPiece|Piece: An abstract class to represent common functionality of all chess pieces]]
$\quad\quad$[[TMP_ChessKing|King: To represent King as a chess piece]]
$\quad\quad$[[TMP_ChessKnight|Knight: To represent Knight as a chess piece]]
$\quad\quad$Similarly, we can create classes for other pieces like **Queen**, **Pawns**, **Rooks**, **Bishops** etc.

$\quad$[[TMP_ChessBoard|Board: To represent a chess board]]
$\quad$[[TMP_ChessPlayer|Player: An abstract class for player, it can be a human or a computer]]
$\quad$[[TMP_ChessMove|Move: To represent a chess move]]
$\quad$[[TMP_ChessGame|Game: To represent a chess game]]