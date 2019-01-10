# random_password_generator
A Python program which generates a random password after the user inputs the desired level of strength and number of characters.
# Generates a password of variable strength and number of characters
import string
import random
a = (string. ascii_letters + string.digits)
b = (string. ascii_letters + string.digits + string.punctuation)
strength = input("How strong would you like your password to be? (strong, medium or weak): ")
strength = (strength.lower())[0]
strength_options = ["s", "m", "w"]
if strength not in strength_options:
 print("Invalid input.")
elif strength in strength_options:
 n = int(input("How many characters would you like your password to be? (1-20): "))
 if n < 1 or n > 20:
   print("Invalid input.")
 elif 1 <= n <= 20:
   if strength == "s":
     print("".join(random.sample(b, n)))
   elif strength == "m":
     print("".join(random.sample(a, n)))
   elif strength == "w":
     print("".join(random.sample(string.ascii_lowercase, n)))
   else:
     print("Invalid input.")
