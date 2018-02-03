# Intro to Programming Workshop
> By the Marianopolis Programming Club
>
> Sunday, February 4, 2018 from 11:00 AM - 12:30 PM.

Here you'll find all the source code from the workshop.

If you have any questions, you can email us at info@marihacks.com.

### Hello world
```python
print("Hello, world.")
```

### Hello, name
```python
name = input("What is your name? ")
print("Hello, %s" % name)
```

### Print empty tic-tac-toe board
```python
# Print an empty board

print("  |  |  ")
print("  |  |  ")
print("  |  |  ")
```
### Add X and O to board
```python
# Create an array of 9 spaces to represent our board
board = [' ']*9
print(board)

# Show change of value
board[0] = 'X'

print("\nLet's play tic tac toe!\n")
print(" %s | %s | %s "  % (board[0],board[1],board[2]))
print(" %s | %s | %s "   % (board[3],board[4],board[5]))
print(" %s | %s | %s \n" % (board[6],board[7],board[8]))
```
### Let user add an X to the board
```python
# Initialize board array
board = [' ']*9

boardPosition = input('Give me a number from 0-8: ')
boardPosition = int(boardPosition)

board[boardPosition] = 'X'

print("\nLet's play tic tac toe!\n")
print(" %s | %s | %s "   % (board[0],board[1],board[2]))
print(" %s | %s | %s "   % (board[3],board[4],board[5]))
print(" %s | %s | %s \n" % (board[6],board[7],board[8]))
```

### Check for winner
```python
# Pick some configuration for board
board = ['X', 'X', 'X',
         'O', 'O', ' ',
         ' ', ' ', ' ' ]

# Print the board
print("\nLet's play tic tac toe!\n")
print(" %s | %s | %s "  % (board[0],board[1],board[2]))
print(" %s | %s | %s "   % (board[3],board[4],board[5]))
print(" %s | %s | %s \n" % (board[6],board[7],board[8]))

# Check if there is a winner
    # You're a winner if you have three spots occupied horizontally, vertically, or diagonally

# Horizontally
if (board[0] == board[1] == board[2] and board[0]!= ' ') or (board[3] == board[4] == board[5] and board[3]!=' ') or (board[6] == board[7] == board[8] and board[0]!=' '):
    print('There is a winner')
```

### Intro to `if` statements
Example together
```python
guess = input("Give me a number between 1 and 5: ")
guess = int(guess)

myNumber = 3

if guess == myNumber:
    print("Yay")
else:
    print("You suck.")
```
[Solution to if statement exercise](https://github.com/marihacks/learnathon-solutions/blob/master/if-statement.md)

### A faster way to check for winner
```python
# Pick some configuration for board
board = ['X', 'X', 'X',
         'O', 'O', ' ',
         ' ', ' ', ' ' ]

# Print the board
print("\nLet's play tic tac toe!\n")
print(" %s | %s | %s "  % (board[0],board[1],board[2]))
print(" %s | %s | %s "   % (board[3],board[4],board[5]))
print(" %s | %s | %s \n" % (board[6],board[7],board[8]))

# Check if there is a winner
    # You're a winner if you have three spots occupied horizontally, vertically, or diagonally

# Horizontally
for i in range(0,7,3):
    if board[i] == board[i+1] == board[i+2] and board[i] != ' ':
        print("There is a winner")
```

### Intro to `for` loops
```python
for i in range(0,100):
    print('Raffi, %i' % i)
```
[Solution to vertical check exercise](https://github.com/marihacks/learnathon-solutions/blob/master/vertical-check.md)

### Checking for diaganol lines
```python
# Pick some configuration for board
board = ['X', 'X', 'X',
         'O', 'O', 'O',
         ' ', ' ', ' ' ]

# Print the board
print("\nLet's play tic tac toe!\n")
print(" %s | %s | %s "  % (board[0],board[1],board[2]))
print(" %s | %s | %s "   % (board[3],board[4],board[5]))
print(" %s | %s | %s \n" % (board[6],board[7],board[8]))

# Check if there is a winner
    # You're a winner if you have three spots occupied horizontally, vertically, or diagonally

# Horizontally
for i in range(0,7,3):
    if board[i] == board[i+1] == board[i+2] and board[i] != ' ':
        print("There is a winner")

# Vertically
for i in range(0,3,1):
    if board[i] == board[i+3] == board[i+6] and board[i] != ' ':
        print("There is a winner")

# Diagonally
if board[0] == board[4] == board[8] and board[0] != ' ':
    print("There is a winner")

if board[2] == board[4] == board[6] and board[2] != ' ':
    print("There is a winner")
```
### A cleaner and more efficient way to organize code
```
Some example here
```

```python
# Minimum number in a list
def minList(inputList):
    currentMin = inputList[0]
    for num in range(1,len(inputList)):
        if inputList[num] < currentMin:
            currentMin = inputList[num]
    return currentMin

# examples
list1 = [-1, 4, 56, -100, 0]
print(minList(list1))
```

### Putting everything into functions
```python

# Pick some configuration for board
board = ['X', 'X', 'X',
         'O', 'O', 'O',
         ' ', ' ', ' ' ]

# Print the board
def print_board(board):
    print("\nLet's play tic tac toe!\n")
    print(" %s | %s | %s "   % (board[0],board[1],board[2]))
    print(" %s | %s | %s "   % (board[3],board[4],board[5]))
    print(" %s | %s | %s \n" % (board[6],board[7],board[8]))

# Check if there is a winner
    # You're a winner if you have three spots occupied horizontally, vertically, or diagonally

# Horizontally
def checkHorizontal(board):
    for i in range(0,7,3):
        if board[i] == board[i+1] == board[i+2] and board[i] != ' ':
            return True

# Vertically
def checkVertical(board):
    for i in range(0,3,1):
        if board[i] == board[i+3] == board[i+6] and board[i] != ' ':
            return True

# Diagonally
def checkDiaganol(board):
    if board[0] == board[4] == board[8] and board[0] != ' ' or (board[2] == board[4] == board[6] and board[2] != ' '):
        return True

# Check if there is a winner using the functions from above
def isWinner(board):
    if checkHorizontal(board) or checkVertical(board) or checkDiaganol(board):
        return True

# Let's try it
if isWinner(board):
    print('There is a winner!')
```
