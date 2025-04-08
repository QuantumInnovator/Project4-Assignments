<!-- Problem Statement
Fill out the double(num) function to return the result of multiplying num by 2. We've written a main() function for you which asks the user for a number, calls your code for double(num) , and prints the result.

Here's a sample run of the program (user input in bold italics):

Enter a number: 2 Double that is 4 -->

def double(num):
    # Multiply num by 2 and return the result
    return num * 2

# Main function to ask user for input and print the doubled value
def main():
    num = int(input("Enter a number: "))  # Ask user for a number
    result = double(num)  # Call double function with the entered number
    print(f"Double that is {result}")  # Print the result

# Call main function to run the program
main()
