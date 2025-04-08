<!-- Problem Statement
Guess My Number

I am thinking of a number between 0 and 99... Enter a guess: 50 Your guess is too high

Enter a new number: 25 Your guess is too low

Enter a new number: 40 Your guess is too low

Enter a new number: 45 Your guess is too low

Enter a new number: 48 Congrats! The number was: 48 -->

import random

# Generate a random number between 0 and 99
number_to_guess = random.randint(0, 99)

def guess_my_number():
    print("I am thinking of a number between 0 and 99...")

    while True:
        # Ask the user to enter a guess
        guess = int(input("Enter a guess: "))

        # Check if the guess is correct, too high, or too low
        if guess > number_to_guess:
            print("Your guess is too high")
        elif guess < number_to_guess:
            print("Your guess is too low")
        else:
            print(f"Congrats! The number was: {number_to_guess}")
            break

# Call the function to start the game
guess_my_number()
