import random

secret_num = random.randint(1,100)
counter = 10

while True:
    try:
        test_num = int(input("Let's find the secret number: "))
        counter -= 1
        if test_num == secret_num:
            print("Bingo! You guessed the number. ")
        if test_num > secret_num:
            print("Sorry, your number is too high. Remaining attempts:  ", counter)
        if test_num < secret_num:
            print("Sorry, your number is too small. Remaining attempts:  ", counter)
        if counter == 0:
            print("Oops, game over! The secret number was: ", secret_num)
    except ValueError:
        print("Please enter a valid number: ")
        continue
