<!-- Problem Statement
We've written a helper function for you called greet(name) which takes as input a string name and prints a greeting. Write some code in main() to get the user's name and then greet them, being sure to call the greet(name) helper function.

Here's a sample run of the program (user input in bold italics):

What's your name? Sophia

Greetings Sophia! -->

# Helper function to greet the user
def greet(name):
    print(f"Greetings {name}!")

# Main function to interact with the user
def main():
    # Prompt the user for their name
    name = input("What's your name? ")
    
    # Call the greet function to greet the user
    greet(name)

# Run the main function
if __name__ == "__main__":
    main()
