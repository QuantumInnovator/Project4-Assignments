<!-- Problem Statement
This program counts the number of times each number appears in a list. It uses a dictionary to keep track of the information.

An example run of the program looks like this (user input is in blue):

Enter a number: 3 Enter a number: 4 Enter a number: 3 Enter a number: 6 Enter a number: 4 Enter a number: 3 Enter a number: 12 Enter a number: 3 appears 3 times. 4 appears 2 times. 6 appears 1 times. 12 appears 1 times. -->

# Create an empty dictionary to store the count of each number
number_counts = {}

while True:
    # Ask the user to enter a number
    user_input = input("Enter a number: ")
    
    # Break the loop if user input is empty
    if user_input == "":
        break
    
    # Convert input to an integer
    number = int(user_input)
    
    # If the number is already in the dictionary, increment its count
    if number in number_counts:
        number_counts[number] += 1
    else:
        # If the number is not in the dictionary, add it with count 1
        number_counts[number] = 1

# Print out the counts of each number
for number, count in number_counts.items():
    print(f"{number} appears {count} times.")
