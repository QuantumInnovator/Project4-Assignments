<!-- Problem Statement
You want to be safe online and use different passwords for different websites. However, you are forgetful at times and want to make a program that can match which password belongs to which website without storing the actual password!

This can be done via something called hashing. Hashing is when we take something and convert it into a different, unique identifier. This is done using a hash function. Luckily, there are several resources that can help us with this.

For example, using a hash function called SHA256(...) something as simple as

hello

can be hashed into a much more complex

2cf24dba5fb0a30e26e83b2ac5b9e29e1b161e5c1fa7425e73043362938b9824

Fill out the login(...) function for a website that hashes their passwords. Login should return True if an email's stored password hash in stored_logins is the same as the hash of password_to_check.

(Hint. You will need to use the provided hash_password(...) function. You don't necessarily need to know how it works, just know that hash_password(...) returns the hash for the password!) -->

import hashlib

# This function simulates the password hashing
def hash_password(password):
    # SHA256 hash function
    return hashlib.sha256(password.encode('utf-8')).hexdigest()

# This is a dictionary where the emails and their hashed passwords are stored
stored_logins = {
    'user1@example.com': hash_password('password123'),
    'user2@example.com': hash_password('mySecureP@ssw0rd'),
    'user3@example.com': hash_password('anotherPassword!'),
}

def login(email, password_to_check):
    # Check if email exists in stored logins
    if email in stored_logins:
        # Compare the stored password hash with the hashed input password
        if stored_logins[email] == hash_password(password_to_check):
            return True  # The passwords match
        else:
            return False  # The passwords don't match
    else:
        return False  # The email is not registered

# Example usage:
email = input("Enter your email: ")
password_to_check = input("Enter your password: ")

if login(email, password_to_check):
    print("Login successful!")
else:
    print("Login failed! Invalid email or password.")
