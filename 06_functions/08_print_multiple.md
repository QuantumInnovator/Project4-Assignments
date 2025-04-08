<!-- Problem Statement
Fill out print_multiple(message, repeats), which takes as parameters a string message to print, and an integer repeats number of times to print message. We've written the main() function for you, which prompts the user for a message and a number of repeats.

Here's a sample run of the program (user input is in blue):

Please type a message: Hello! Enter a number of times to repeat your message: 6 Hello! Hello! Hello! Hello! Hello! Hello! -->

# Function to print the message multiple times
def print_multiple(message, repeats):
    for _ in range(repeats):  # Loop to repeat the message
        print(message)

# Main function to get user input and call the print_multiple function
def main():
    # Ask user to enter a message
    message = input("Please type a message: ")
    
    # Ask user to enter the number of times to repeat the message
    repeats = int(input("Enter a number of times to repeat your message: "))
    
    # Call the print_multiple function to print the message the specified number of times
    print_multiple(message, repeats)

# Run the main function
if __name__ == "__main__":
    main()
