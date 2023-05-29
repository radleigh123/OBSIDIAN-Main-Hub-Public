**Board.java**
This Java source code represents a chess board. The `Board` class contains various methods and variables for managing and displaying the chess board.

Let's go through the code step by step:
-   The code begins with the package declaration `package src;` and import statement `import src.chess_pieces.*;` to include the necessary classes.
-   The `Board` class is declared with several private instance variables:
    -   `boardType`: A character representing the type of the board.
    -   `boardRw`: An integer representing the number of rows on the board.
    -   `boardClmn`: An integer representing the number of columns on the board.
    -   `dispBoxes`: A 2-dimensional char array representing the display boxes on the board.
    -   `boxes`: A 2-dimensional array of `Spot` objects representing the spots on the board.
-   The class provides two constructors:
    -   `public Board()`: A default constructor with no parameters.
    -   `public Board(String boardType)`: A constructor that takes a `boardType` as a string parameter. It initializes the `boardType` variable and calls the `getBoardType()` method.
-   Next, there are getter and setter methods for the `boardRw`, `boardClmn`, `dispBoxes`, and `boardType` variables.
-   The `startBoard()` method is the main focus of this explanation. It initializes the chess board based on the `boardType`. It uses a `switch` statement with `boardType` converted to lowercase to determine the type of the board.
    -   Case 'a': This represents a 3x4 chess board. It sets the `boardRw` and `boardClmn` to 4 and 3, respectively. It initializes the `dispBoxes` array with the initial configuration of the board and assigns specific chess pieces to the `boxes` array.
    -   Case 'b': This represents a 4x5 chess board. It sets the `boardRw` and `boardClmn` to 5 and 4, respectively. It initializes the `dispBoxes` array with the initial configuration of the board and assigns specific chess pieces to the `boxes` array.
    -   Case 'c': This represents a 5x5 chess board. It sets the `boardRw` and `boardClmn` to 5 and 5, respectively. It initializes the `dispBoxes` array with the initial configuration of the board and assigns specific chess pieces to the `boxes` array.
    -   Default case: If the `boardType` is not 'a', 'b', or 'c', it prints "INVALID" to indicate an invalid board type.
-   The `displayBoard()` method is responsible for displaying the chess board on the console. It prints the board with appropriate labels for rows and columns. The `dispBoxes` array is used to display the current state of the board.
-   The `resetBoard()` method sets both `dispBoxes` and `boxes` to `null`, effectively resetting the board.

**GameStatus.java**
An enumeration is a special type in Java that represents a fixed set of named values. In this case, the `GameStatus` enumeration defines three possible game statuses:
1.  `ACTIVE`: This status indicates that the game is currently active and ongoing.
2.  `BLACK_WIN`: This status indicates that the game has ended, and the black player has won.
3.  `WHITE_WIN`: This status indicates that the game has ended, and the white player has won.

**Piece.java**
The abstract class `Piece` will serve as a base class for different types of chess pieces. Abstract classes in Java cannot be instantiated directly but are meant to be extended by other classes.

The `Piece` class has a private boolean variable `white` that represents whether the piece is white or black. By default, the `white` variable is set to `false` (black piece).
-   The class has a constructor that takes a boolean parameter `w`, which is used to set the `white` variable.
-   The `canMove()` method is responsible for determining whether a piece can move from the starting spot to the ending spot on the given board. The implementation of this method will vary depending on the specific chess piece. For example...

---

**Bishop.java**
The `Bishop` class represents a bishop chess piece. It extends a "Piece" class and has a override method called `canMove` that determines if the bishop can move from a starting spot to an ending spot on a chessboard. The method checks if the path is clear and if the move is diagonal. If both conditions are met, the method returns true; otherwise, it returns false.

**King.java**
The class implements the logic for determining whether a king chess piece can move from a start position to an end position on a given chessboard, taking into account the piece's color, the presence of other pieces on the destination spot, the maximum movement range of a king, and the safety of the king after the move.

The `isKingSafe` method takes a "Board" object and a boolean flag "isWhite" indicating the color of the king. It searches for the king's current position on the board and assigns it to the "kingSpot" variable. Then, it iterates over all the spots on the board to find any opponent's piece that can attack the king. If such a piece is found, the method returns false, indicating that the king would be under attack if the move is made.

After checking all the spots on the board, if no attacking piece is found, the method returns true, indicating that the king would be safe after the move.

**Knight.java**
This implements the logic for determining whether a knight chess piece can move from a start position to an end position on a given chessboard, taking into account the piece's color, the presence of other pieces on the destination spot, and the specific L-shaped movement pattern of a knight.

**Pawn.java**
The pawn chess piece can move from a start position to an end position on a given chessboard, taking into account the piece's color, the presence of other pieces on the destination spot, the specific movement patterns of pawns (including the ability to move forward, capture diagonally, and move only one step at a time), and the different movement rules for white, as they can only move forward and black pawns, where they can only move backward.

**Queen.java**
The queen chess piece can move from a start position to an end position on a given chessboard and while having the movement patterns of a queen (including horizontal, vertical, and diagonal movements) while also checking for any blocking pieces along the its path.

**Rook.java**
This class represents the rook chess piece that can move horizontally or vertically, taking into account the piece's color, the presence of other pieces on the destination spot, and also checking for any blocking pieces along the path.

**Game.java**
1.  Package and Imports: The code is in the "src" package, and it imports the ArrayList and Scanner classes from the Java util package.
2.  Class Declaration: The code defines a public class named "Game."
3.  Instance Variables: The class has various instance variables representing different aspects of the game, including:
    -   `Scanner sc`: A Scanner object used for input.
    -   `Player[] players`: An array to store two Player objects.
    -   `HumanPlayer player1, player2`: Two specific types of Player objects.
    -   `Player currentTurn`: The current player's turn.
    -   `ArrayList<HumanPlayer> playersList`: An ArrayList to store HumanPlayer objects.
    -   `Board board`: An instance of the Board class.
    -   `GameStatus status`: The status of the game.
    -   `char[] availPieces`: An array to store available pieces.
    -   `char inputPiece`: The selected piece input by the user.
    -   `String inputPieceName`: The name of the selected piece.
    -   `boolean isInputPieceValid, isInputDuplicateValid, isPieceMoveValid, isInputMoveValid`: Flags to check the validity of input and moves.
    -   `int startRw, startClmn, endRw, endClmn`: Variables to store row and column coordinates for move positions.
4.  Getters and Setters: Public methods to access and modify the instance variables.
5.  initialize Method: Initializes the game by assigning sides to players and starting the board.
6.  `updatePlayers` Method: Updates the player statistics based on the provided `HumanPlayer` objects.
7.  `checkPieces` Method: Displays the uncaptured pieces for the current turn's player.
8.  `checkDuplicate` Method: Checks if there are duplicate pieces on the board for the selected piece.
9.  `displayStats` and displayStats2 Methods: Display various statistics related to the game.
10.  `playerMove` Method: Executes a move for a player based on the provided positions.
11.  The `makeMove` method is responsible for executing a move in the game. It takes a `Move` object and a `Player` object as parameters. Here's a breakdown of what the method does:
>[!INFO|clean no-t]
> 1.  It first retrieves the source piece from the starting spot of the move using `move.getStart().getPiece()`. If the source piece is `null`, it means the starting spot is empty, and the method returns `false`.
> 2. Next, it performs several validity checks to ensure that the move is valid and follows the rules of the game:
> 	-   It checks if the current player making the move (`player`) is the same as the current turn (`currentTurn`). If they are not the same, it means it's not the player's turn, and the method returns `false`.
> 	-   It checks if the color of the source piece (`sourcePiece`) matches the color of the player making the move (`player`). If they do not match, it means the player is trying to move the opponent's piece, and the method returns `false`.
> 	-   It calls the `canMove` method on the source piece to check if the specific piece movement is valid according to the game's rules. If the move is not valid, the method returns `false`.
> 3. If all the validity checks pass, the method proceeds with executing the move:
> -   It sets the piece in the ending spot of the move (`move.getEnd()`) to be the same as the piece in the starting spot (`move.getStart().getPiece()`).
> -   It sets the piece in the starting spot to `null`, indicating that it has been moved.
> -   It updates the display boxes on the board to reflect the move.
> 3. Finally, the method switches the current turn to the other player. If the current turn is `players[0]`, it is set to `players[1]`, and vice versa.
> 
> The `makeMove` method returns `true` if the move is successfully executed, and `false` if any of the validity checks fail.

12.  `game` Method: Starts the game by initializing the board and getting player information.
13.  `game2` Method: Executes the main logic of the game, including piece selection, move validation, and capturing pieces.