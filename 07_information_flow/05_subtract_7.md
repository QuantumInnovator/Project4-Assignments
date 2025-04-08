<!-- Problem Statement
Fill out the subtract_seven helper function to subtract 7 from num, and fill out the main() method to call the subtract_seven helper function! If you're stuck, revisit the add_five example from lecture. -->

# Helper function to subtract 7 from the given number
def subtract_seven(num):
    return num - 7

# Main function to prompt the user for a number and call subtract_seven
def main():
    # Ask the user to enter a number
    num = int(input("Enter a number: "))
    
    # Call subtract_seven to subtract 7 from the input number
    result = subtract_seven(num)
    
    # Print the result
    print(f"Result after subtracting 7: {result}")

# Call the main function to run the program
if __name__ == "__main__":
    main()
