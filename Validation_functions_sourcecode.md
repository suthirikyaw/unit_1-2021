```.py
#Name of file is Validation.py
def validationTwo(choice):
    while choice != 1 or choice !=2:
        if choice == 1:
            return 1
        elif choice == 2:
            return 2
        else:
            print("Please only enter 1 or 2.")
            choice = int(input(">> "))

def validationThree(choice):
    while choice != 1 or choice !=2 or choice !=3:
        if choice == 1:
            return 1
        elif choice == 2:
            return 2
        elif choice == 3:
            return 3
        else:
            print("Please only enter 1, 2, or 3.")
            choice = int(input(">> "))

