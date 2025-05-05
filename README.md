# Rock-Paper-Scissors

# Rock, Paper, Scissors ✊✋✌️ (Python Learning Project)

This project is part of my Python learning journey! In this exercise, I built a Rock, Paper, Scissors game where the computer and user make random choices, and the game determines who wins.

---

## 🧠 What I Learned

### ✅ Lists Are Powerful
I learned how to use **lists to store multiple related items**, like the ASCII art for rock, paper, and scissors. This helped me **shorten my code** and keep it cleaner.

### ✅ Simplifying with Numbers
Instead of repeating a lot of similar `if` statements, I learned I could **convert input choices to numbers** (like `1` for rock, `2` for paper, etc.), and **compare them using logic**. This reduces repetition and makes the code easier to maintain and expand.

---

## 🎮 How It Works

- The user selects Rock (1), Paper (2), or Scissors (3).
- The computer randomly chooses one of the options.
- The program compares both and prints who won.

### Code Snippet (Preview)

```python
import random
print("Lets play rock, paper, scissors")

rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''
cpu_choice = random.choice([rock, paper, scissors])
your_choice = input("Select 1 for rock, 2 for paper or 3 for scissors\n")
if your_choice == "1":
    print(rock)
    print("Computer chose: \n", cpu_choice)
    if cpu_choice == scissors:
        print("You Win!!!")
    elif cpu_choice == rock:
        print("Draw")
    else:
        print("You Lose!!")

elif your_choice == "2":
    print(paper)
    print("Computer chose: \n", cpu_choice)
    if cpu_choice == rock:
        print("You Win!!!")
    elif cpu_choice == paper:
        print("Draw")
    else:
        print("You Lose!!")

else:
    print(scissors)
    print("Computer chose: \n", cpu_choice)
    if cpu_choice == paper:
        print("You Win!!!")
    elif cpu_choice == scissors:
        print("Draw")
    else:
        print("You Lose!!")
----------------------------------------------------------------------------
game_images = [rock, paper, scissors]

user_choice = int(input("Select 0 for rock, 1 for paper or 2 for scissors\n"))
if user_choice >= 0 and user_choice <= 2:
    print(game_images[user_choice])

computer_choice = random.randint(0,2)
print("Computer chose:")
print(game_images[computer_choice])

if user_choice >= 3 or user_choice < 0:
    print("You typed an invalid number! You lose!")
elif user_choice == 0 and computer_choice == 2:
    print("You Win")
elif computer_choice > user_choice:
    print("You Lose")
elif computer_choice == user_choice:
    print("It's a draw!")
elif computer_choice == 0 and user_choice == 2:
    print("You Lose!")
elif user_choice >computer_choice:
    print("You Win!")
