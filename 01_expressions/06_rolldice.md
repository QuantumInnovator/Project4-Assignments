<!-- Simulate rolling two dice, and prints results of each roll as well as the total.
 -->


import random  # Importing random module to simulate dice rolls

# Simulate rolling two dice
roll1 = random.randint(1, 6)  # First dice roll (between 1 and 6)
roll2 = random.randint(1, 6)  # Second dice roll (between 1 and 6)

# Calculate total of the two rolls
total = roll1 + roll2

# Print the results
print("Dice 1 rolled:", roll1)
print("Dice 2 rolled:", roll2)
print("Total of both rolls:", total)
