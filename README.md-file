import random
import string

def check_strength(password):
    length = len(password)
    has_upper = any(c.isupper() for c in password)
    has_lower = any(c.islower() for c in password)
    has_digit = any(c.isdigit() for c in password)
    has_symbol = any(c in string.punctuation for c in password)

    score = has_upper + has_lower + has_digit + has_symbol

    if length < 6:
        return "Weak"
    elif score >= 3 and length >= 8:
        return "Strong"
    elif score >= 2:
        return "Medium"
    else:
        return "Weak"

def generate_password(length=12):
    chars = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choice(chars) for _ in range(length))
    return password


print("===== PASSWORD TOOL =====")
print("1. Check Password Strength")
print("2. Generate Strong Password")

choice = int(input("Enter your choice (1/2): "))

if choice == 1:
    pwd = input("Enter your password: ")
    strength = check_strength(pwd)
    print("Password Strength:", strength)

elif choice == 2:
    length = int(input("Enter password length (8-20 recommended): "))
    pwd = generate_password(length)
    print("Generated Strong Password:", pwd)

else:
    print("Invalid choice. Please run again.")
