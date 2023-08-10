- 👋 Hi, I’m @huzaifawaf
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
huzaifawaf/huzaifawaf is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
class ChessGame:
    def __init__(self):
        self.board = [
            ['R', 'N', 'B', 'Q', 'K', 'B', 'N', 'R'],
            ['P', 'P', 'P', 'P', 'P', 'P', 'P', 'P'],
            [' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '],
            [' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '],
            [' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '],
            [' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '],
            ['p', 'p', 'p', 'p', 'p', 'p', 'p', 'p'],
            ['r', 'n', 'b', 'q', 'k', 'b', 'n', 'r']
        ]
        self.current_player = 'white'

    def print_board(self):
        for row in self.board:
            print(' '.join(row))
    
    def get_move(self):
        from_square = input(f"{self.current_player.capitalize()}'s move: Enter the source square (e.g., 'e2'): ")
        to_square = input("Enter the destination square: ")
        return from_square, to_square
    
    def is_valid_move(self, from_square, to_square):
        # Add validation logic here
        return True
    
    def make_move(self, from_square, to_square):
        # Add move logic here
        pass
    
    def play(self):
        while True:
            self.print_board()
            from_square, to_square = self.get_move()
            
            if not self.is_valid_move(from_square, to_square):
                print("Invalid move. Try again.")
                continue
            
            self.make_move(from_square, to_square)
            self.current_player = 'black' if self.current_player == 'white' else 'white'
            
            # Add checkmate and stalemate conditions here

if __name__ == "__main__":
    game = ChessGame()
    game.play()
