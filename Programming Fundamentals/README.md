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
