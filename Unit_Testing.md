```.py

def validationTwo(choice):
    while choice != 1 or choice !=2:
        if choice == 1:
            return 1
        elif choice == 2:
            return 2
        else:
            print("Please only enter 1 or 2.")
            choice = int(input(">> "))


print(validationTwo(1))
print(validationTwo(2))
print(validationTwo(3))

C:\Users\ASUS\PycharmProjects\pythonProject2\venv\Scripts\python.exe C:/Users/ASUS/PycharmProjects/pythonProject2/main.py
1
2
Please only enter 1 or 2.
>> 

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
