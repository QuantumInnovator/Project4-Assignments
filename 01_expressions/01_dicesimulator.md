<!-- Problem Statement
Simulate rolling two dice, three times. Prints the results of each die roll. This program is used to show how variable scope works. -->

import random

def roll_dice():
    die1 = random.randint(1, 6)
    die2 = random.randint(1, 6)
    print("Die 1:", die1, "Die 2:", die2)

# Roll the dice 3 times
roll_dice()
roll_dice()
roll_dice()
