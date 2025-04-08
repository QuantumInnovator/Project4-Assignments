<!-- Problem Statement
Write a program which continuously asks the user to enter values which are added one by one into a list. When the user presses enter without typing anything, print the list.

Here's a sample run (user input is in blue):

Enter a value: 1 Enter a value: 2 Enter a value: 3 Enter a value: Here's the list: ['1', '2', '3'] -->

# Initialize an empty list to store user input
user_list = []

# Continuously ask the user for input
while True:
    value = input("Enter a value: ")
    
    # If the user presses Enter without typing anything, exit the loop
    if value == "":
        break
    
    # Append the entered value to the list
    user_list.append(value)

# Print the list when the user presses Enter without input
print("Here's the list:", user_list)
