# Vertical Check Solution
```python
# Pick some configuration for board
board = ['X', 'X', 'X',
         'O', 'O', ' ',
         ' ', ' ', ' ' ]

# Print the board
print("\nLet's play tic tac toe!\n")
print(" %s | %s | %s "   % (board[0],board[1],board[2]))
print(" %s | %s | %s "   % (board[3],board[4],board[5]))
print(" %s | %s | %s \n" % (board[6],board[7],board[8]))

# Check if there is a winner
# You're a winner if:
    #You have three spots occupied horizontally, vertically, or diagonally

# Horizontally
for i in range(0,7,3):
    if board[i] == board[i+1] == board[i+2] and board[i] != ' ':
        print('There is a winner')

# Vertically
for i in range(0,3,1):
    if board[i] == board[i+3] == board[i+6] and board[i] != ' ':
        print('There is a winner')
```
[Back to learnathon workshop](https://github.com/marihacks/learnathon)
