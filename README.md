# python-program
python tic-tac-toe

import random



def NewGame(self):
        self.GameBoard = [" "," "," "," "," "," "," "," "," "]

        self.PlayerPiece = "O"
        self.OpponentPiece = "X"
        

def Move(self, MoveFromOpponent):
    MOveCount = 2
    if MoveFromOpponent == 0:
        MyMove = 1
        MoveCount += 2
        self.PlayerPiece = "X"
        self.OpponentPiece = "O"
            
    self.GameBoard[MyMove - 1] = self.PlayerPiece
    return MyMove
    
    self.GameBoard[MoveFromOpponent - 1] = self.OpponetPiece
       
        
    MyMove = random.randint(1,9)

        
    while self.GameBoard[MyMove - 1] != " ":
        MyMove = random.randint(1,9)
        
    self.GameBoard[MyMove - 1] = self.PlayerPiece
    return MyMove
        
        

class TicTacToe_Keyboard:


    def PrintBoard(CurrentBoard):
        print(CurrentBoard.GameBoard[0] + " | " + CurrentBoard.GameBoard[1] + " | " + CurrentBoard.GameBoard[2])
        print("--+---+--")
        print(CurrentBoard.GameBoard[3] + " | " + CurrentBoard.GameBoard[4] + " | " + CurrentBoard.GameBoard[5])
        print("--+---+--")
        print(CurrentBoard.GameBoard[6] + " | " + CurrentBoard.GameBoard[7] + " | " + CurrentBoard.GameBoard[8])
        print("")


def CheckForWin(CurrentBoard):
    Pieces = ["X", "O"]

    for Piece in Pieces:
        if CurrentBoard.GameBoard[0] == Piece and CurrentBoard.GameBoard[1] == Piece and CurrentBoard.GameBoard[2] == Piece:
            return Piece
    
        if CurrentBoard.GameBoard[3] == Piece and CurrentBoard.GameBoard[4] == Piece and CurrentBoard.GameBoard[5] == Piece:
            return Piece
    
        if CurrentBoard.GameBoard[6] == Piece and CurrentBoard.GameBoard[7] == Piece and CurrentBoard.GameBoard[8] == Piece:
            return Piece
    
        if CurrentBoard.GameBoard[0] == Piece and CurrentBoard.GameBoard[3] == Piece and CurrentBoard.GameBoard[6] == Piece:
            return Piece
    
        if CurrentBoard.GameBoard[1] == Piece and CurrentBoard.GameBoard[4] == Piece and CurrentBoard.GameBoard[7] == Piece:
            return Piece
    
        if CurrentBoard.GameBoard[2] == Piece and CurrentBoard.GameBoard[5] == Piece and CurrentBoard.GameBoard[8] == Piece:
            return Piece
    
        if CurrentBoard.GameBoard[0] == Piece and CurrentBoard.GameBoard[4] == Piece and CurrentBoard.GameBoard[8] == Piece:
            return Piece
    
        if CurrentBoard.GameBoard[2] == Piece and CurrentBoard.GameBoard[4] == Piece and CurrentBoard.GameBoard[6] == Piece:
            return Piece
    
    if CurrentBoard.GameBoard.count(" ") == 0:
        
        return "D"
    
    return " "


def PlayGame():
    Players = [Player2, Player1]



CurrentMove = Player1.Move(0)
PrintBoard(Player1)

while True:
    for Player in Players:
        CurrentMove = Player.Move(CurrentMove)
        PrintBoard(Player)
        
        AnyoneWon = CheckForWin(Player)
        if AnyoneWon != " ":
            break

    if AnyoneWon != " ":
        print("Winner: " + AnyoneWon)
        break

Player1 = TicTacToe_Random()
Player1.NewGame()

Player2 = TicTacToe_Keyboard()
Player2.NewGame()

PlayGame()
