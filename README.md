# Guess the Number Game

## Description
Guess the Number is a classic single-player game where the computer generates a random number between 1 and 100, and the player attempts to guess it. The game provides feedback after each guess, indicating whether the guess was too high or too low, until the player correctly identifies the number. This implementation includes a maximum attempt limit to add challenge to the game.

## Features
- Random number generation between 1 and 100
- Real-time feedback on guesses (too high/too low)
- Maximum attempt limit (5 tries)
- Victory message with the number of attempts made
- Game over message revealing the secret number when attempts are exhausted

## How to Play
1. Run the Python script
2. Enter your guess when prompted
3. Receive feedback on whether your guess is too high or too low
4. Continue guessing until you either:
   - Guess the correct number (win)
   - Reach the maximum number of attempts (lose)

## Code
Solution is written inside the Jupyter Notebook : [View the code ](Basics_Checkpoint.ipynb)
```python
import random as rnd

f= rnd.randint(1,100)
r = int (input('Enter a number between 1 and 100'))
Try = 0 

while True :

    if (r > f ):
        print('Too hight try again ')
        r = int (input('Enter a number between 1 and 100'))
        Try = Try +1

    if (r < f ):
        print('Too low try again ')
        r = int (input('Enter a number between 1 and 100'))
        Try = Try + 1
         
    if (Try == 5): 
        print(f'You reach the maximum number of tries, the number was {f}, better luck next time !')
        break
   
    if (r == f):
        print(f"YOU GOT THE RIGHT NUMBER AT TRY NUMBER {Try+1}")
        break

```

## Welcome to the Guess the Number game!

I'm thinking of a number between 1 and 100.
Can you guess what it is?

Enter your guess: 50
Your guess is too high.
Guess again.

Enter your guess: 25
Your guess is too low.
Guess again.

Enter your guess: 37
Your guess is too high.
Guess again.

Enter your guess: 31
Congratulations! You guessed the number correctly!
    if r == f:
        print(f"YOU GOT THE RIGHT NUMBER AT TRY NUMBER {Try + 1}")
        break
