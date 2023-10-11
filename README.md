from random import randrange
from time import sleep

print("Welcome to rock paper scissor game!")
print("Type any number from 1 to 3 in order to play.")
print("rock(1),paper(2),scissor(3).")

while True:  # while loop
    a = int(input("Your element is? "))
    sleep(0.5)
    if a == 1:
        print("You: rock")
    elif a == 2:
        print("You: paper")
    elif a == 3:
        print("You: scissor")
    else:
        print("Error! Please type correct number.")
        break

    b = randrange(1, 3)
    if b == 1:
        print("Computer: rock")
    elif b == 2:
        print("Computer: paper")
    elif b == 3:
        print("Computer: scissor")
    sleep(0.5)

    if a == b: print("Draw!")  # outcome
    if a == 1 and b == 2:
        print("You lost!")
    elif a == 1 and b == 3:
        print("You won!")
    elif a == 2 and b == 1:
        print("You won!")
    elif a == 2 and b == 3:
        print("You lost!")
    elif a == 3 and b == 1:
        print("You lost!")
    elif a == 3 and b == 2:
        print("You won!")

    sleep(0.5)
    c = str(input("Do you wanna countinue? (y/n)"))
    if c == "y" or c == "Y":
        continue
    elif c == "n" or c == "N":
        print("Thanks for playing!")
        break
    else:
        print("Error!")
        break

