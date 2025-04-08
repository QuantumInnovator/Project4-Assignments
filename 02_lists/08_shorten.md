<!-- Problem Statement
Fill out the function shorten(lst) which removes elements from the end of lst, which is a list, and prints each item it removes until lst is MAX_LENGTH items long. If lst is already shorter than MAX_LENGTH you should leave it unchanged. We've written a main() function for you which gets a list and passes it into your function once you run the program. For the autograder to pass you will need MAX_LENGTH to be 3, but feel free to change it around to test your program. -->

MAX_LENGTH = 3  # Set the maximum length of the list

def shorten(lst):
    # Check if the list length is greater than MAX_LENGTH
    while len(lst) > MAX_LENGTH:
        removed_item = lst.pop()  # Remove the last item from the list
        print(f"Removed: {removed_item}")  # Print the removed item

def main():
    # Example list to test
    lst = [1, 2, 3, 4, 5]
    
    print(f"Original list: {lst}")
    shorten(lst)  # Call the shorten function
    print(f"List after shortening: {lst}")

# Run the main function to test the program
main()
