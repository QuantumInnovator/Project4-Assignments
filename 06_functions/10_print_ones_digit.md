<!-- Problem Statement
Write a function called print_ones_digit , which takes as a parameter an integer num and prints its ones digit. The modulo (remainder) operator, %, should be helpful to you here. Call your function from main()!

Here's a sample run (user input is in blue):

Enter a number: 42 The ones digit is 2 -->

# Function to print the ones digit of a given number
def print_ones_digit(num):
    # Using the modulo operator to find the ones digit
    ones_digit = num % 10
    print(f"The ones digit is {ones_digit}")

# Main function to interact with the user
def main():
    # Prompt user for an integer
    num = int(input("Enter a number: "))
    
    # Call the function to print the ones digit
    print_ones_digit(num)

# Run the main function
if __name__ == "__main__":
    main()
