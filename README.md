import random
numbers=['0','1','2','3','4','5','6','7','8','9']
letters=['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
symbols=['!','@','#','$','%','^','&','*','=']
print("welcome to the password generator!")
number_of_letters=int(input("How many letters would you like in your password?\n"))
number_of_numbers=int(input("How many numbers would you like in your password?\n"))
number_of_symbols=int(input("How many symbols would you like in your password?\n"))
password=""
for char in range(1,number_of_letters + 1):
    password+=random.choice(letters)
for char in range(1,number_of_numbers+1):
    password+=random.choice(numbers)
for char in range(1,number_of_symbols+1):
    password+=random.choice(symbols)
password_list = list(password)
random.shuffle(password_list)
final_password = ''.join(password_list)
print(f"Your generated password is: {final_password}")
