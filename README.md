# Password-Generator
import random
letters = ['A','B','C','D','E','F','G','H','I','J','K','L','M','N','O','P','Q','R','S','T','U','V','W','X','Y','Z',
           'a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z']
numbers = ['1','2','3','4','5','6','7','8','9','0']
symbols = ['!','@','#','$','%','^','&','*','()','+','-']
print("Welcome to Password Generator...!")
n_letter = int(input("Enter the number of letters required in your password: "))
n_numbers = int(input("Enter the number of numbers required in your password: "))
n_symbols = int(input("Enter the number of Symbols required in your password: "))
password = ""
password_list = []
for i in range(1,n_letter+1):
    char = random.choice(letters)
    password_list += char
for i in range(1,n_numbers+1):
    char = random.choice(numbers)
    password_list += char
for i in range(1,n_symbols+1):
    char = random.choice(symbols) 
    password_list += char
random.shuffle(password_list)
for char in password_list:
    password += char
print("Here is your Generated password : ")
print(password)
