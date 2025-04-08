<!-- Problem Statement
Fill out the function count_even(lst) which

first populates a list by prompting the user for integers until they press enter (please use the prompt "Enter an integer or press enter to stop: "),

and then prints the number of even numbers in the list.

If you'd prefer to focus on the second task only, scroll down for our implementation of the first task! -->

def count_even(lst):
    # Populate the list by prompting the user for integers
    while True:
        user_input = input("Enter an integer or press enter to stop: ")
        
        if user_input == "":  # Stop if the user presses Enter without typing anything
            break
        
        try:
            # Convert the input to an integer and add it to the list
            number = int(user_input)
            lst.append(number)
        except ValueError:
            print("That's not a valid integer. Please try again.")

    # Count the number of even numbers in the list
    even_count = sum(1 for num in lst if num % 2 == 0)
    
    # Print the number of even numbers
    print(f"The number of even numbers in the list is: {even_count}")

# Example of calling the function
numbers = []
count_even(numbers)
