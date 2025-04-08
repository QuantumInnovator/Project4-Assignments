<!-- Problem Statement
Fill out the get_name() function to return your name as a string! We've written a main() function for you which calls your function to retrieve your name and then prints it in a greeting.

Here's a sample run of the program where the name we've decided to return is Sophia (the autograder expects the returned name to be Sophia):

Howdy Sophia ! 🤠 -->

def get_name():
    # Return your name as a string
    return "Sophia"

# Main function to print a greeting using the name returned by get_name()
def main():
    name = get_name()  # Call get_name function to get the name
    print(f"Howdy {name} ! 🤠")  # Print the greeting with the returned name

# Call main function to run the program
main()
