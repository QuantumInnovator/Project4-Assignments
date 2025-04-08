<!-- Problem Statement
In this program we show an example of using dictionaries to keep track of information in a phonebook. -->

# Initialize an empty dictionary to store the phonebook
phonebook = {}

def add_contact(name, number):
    """Function to add a new contact to the phonebook."""
    phonebook[name] = number
    print(f"Contact for {name} added.")

def search_contact(name):
    """Function to search for a contact in the phonebook."""
    if name in phonebook:
        print(f"{name}'s phone number is {phonebook[name]}")
    else:
        print(f"{name} not found in the phonebook.")

def display_contacts():
    """Function to display all contacts in the phonebook."""
    if phonebook:
        print("\nPhonebook Contacts:")
        for name, number in phonebook.items():
            print(f"{name}: {number}")
    else:
        print("No contacts in the phonebook.")

# Main program loop
while True:
    print("\nPhonebook Menu:")
    print("1. Add a contact")
    print("2. Search for a contact")
    print("3. Display all contacts")
    print("4. Exit")
    
    choice = input("Choose an option (1/2/3/4): ")
    
    if choice == '1':
        name = input("Enter the name of the contact: ")
        number = input("Enter the phone number: ")
        add_contact(name, number)
        
    elif choice == '2':
        name = input("Enter the name of the contact to search: ")
        search_contact(name)
        
    elif choice == '3':
        display_contacts()
        
    elif choice == '4':
        print("Exiting phonebook.")
        break
        
    else:
        print("Invalid choice. Please choose again.")
