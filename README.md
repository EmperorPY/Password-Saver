This simple program creates a file for your passwords. The text file is saved as passwords.txt
WARNING: This file is not encrypted and isnt safe to cyber attacks to your computer. 
Use at your own risk
Code:
-
print("Welcome to the password manager")
while True:
    enter_location = input("What app/website is this password for?").strip()
    enter_password = input("Enter the password\n>")
    with open("passwords.txt", "a") as file:
        file.write(f"Location: {enter_location}\n Password: {enter_password}")
    repeat = input("Do you want to add another? (Y/N)").strip().upper()
    if repeat == ("Y"):
        continue
    else:
        print("Thank-you! Your passwords are now saved in the passwords.txt file on your computer.")
        break
