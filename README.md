#-------------------------------------------------------------------------------
# Name:        ROCK PAPER SCISSORS GAME
# Purpose:     Cod Soft TASK-4
# Rock-Paper-Scissors Game, User Input: Prompt the user to choose rock, paper, or scissors. Computer Selection: Generate a random choice (rock, paper, or scissors) for the computer. Game Logic: Determine the winner based on the user's choice and the computer's choice. Rock beats scissors, scissors beat paper, and paper beats rock. Display Result: Show the user's choice and the computer's choice. Display the result, whether the user wins, loses, or it's a tie. Score Tracking (Optional): Keep track of the user's and computer's scores for multiple rounds. Play Again: Ask the user if they want to play another round. User Interface: Design a user-friendly interface with clear instructions and feedback.
# Author:      NURFUL SHAIKH
# Created:     07-11-2023
#-------------------------------------------------------------------------------
import random
print('Winning rules of the game ROCK PAPER SCISSORS are :\n'
      + "Rock vs Paper -> Paper wins \n"
      + "Rock vs Scissors -> Rock wins \n"
      + "Paper vs Scissors -> Scissor wins \n")
while True:
    print("Enter your choice \n 1 - Rock \n 2 - Paper \n 3 - Scissors \n")
    choice=int(input("Enter your choice :"))
    while choice > 3 or choice <1:
      choice=int(input('Enter a valid choice please ☺'))
    if choice == 1:
        choice_name= 'Rock'
    elif choice == 2:
        choice_name= 'Paper'
    else:
        choice_name= 'Scissors'
    print('User choice is \n',choice_name)
    print('Now its Computers Turn....')
    comp_choice = random.randint(1,3)
    while comp_choice == choice:
        comp_choice = random.randint(1,3)
    if comp_choice == 1:
        comp_choice_name = 'rocK'
    elif comp_choice == 2:
        comp_choice_name = 'papeR'
    else:
        comp_choice_name = 'scissoR'
    print("Computer choice is \n", comp_choice_name)
    print(choice_name,'Vs',comp_choice_name)
    if choice == comp_choice:
        print('Its a Draw',end="")
        result="DRAW"
    if (choice==1 and comp_choice==2):
        print('paper wins =>',end="")
        result='papeR'
    elif (choice==2 and comp_choice==1):
        print('paper wins =>',end="")
        result='Paper'
    if (choice==1 and comp_choice==3):
        print('Rock wins =>\n',end= "")
        result='Rock'
    elif (choice==3 and comp_choice==1):
        print('Rock wins =>\n',end= "")
        result='rocK'
    if (choice==2 and comp_choice==3):
        print('Scissors wins =>',end="")
        result='scissoR'
    elif (choice==3 and comp_choice==2):
        print('Scissors wins =>',end="")
        result='Rock'
    if result == 'DRAW':
        print("<== Its a tie ==>")
    if result == choice_name:
        print("<== User wins ==>")
    else:
        print("<== Computer wins ==>")
    print("Do you want to play again? (Y/N)")
    ans = input().lower
    if ans =='n':
        break
print("thanks for playing")
