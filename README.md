# randompass
import random
import pyautogui

character="0123456789abcdefghijklmnopqrsruvwxyz@#."
character_list=list(character)

password=pyautogui.password("Enter The Password Here: ")
guess_password=''
while (guess_password!=password):
    guess_password=random.choices(character_list,k=len(password))

    print(""+str(guess_password))
    if (guess_password==list(password)):
        print("".join(guess_password))
