```.py

#Testing if the validation system only takes 1 and 2
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

#OUTPUT
C:\Users\ASUS\PycharmProjects\pythonProject2\venv\Scripts\python.exe C:/Users/ASUS/PycharmProjects/pythonProject2/main.py
1
2
Please only enter 1 or 2.
>> 

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
#Testing if the ending successfully encodes and stores the usernames
def ending(score, time):
    shift = 3
    name = input("Please enter your username to record your score. \n"
                 ">> ")
    #caesars_cypher to encode the username
    encoded_name = ''
    for i in range(len(name)):
        letter = name[i]
        letter_code = ord(letter)
        shifted_code = letter_code + shift
        if (shifted_code > 122 and letter.islower()) or (shifted_code > 90 and letter.isupper()):
            shifted_code -= 26
        encoded_name += chr(shifted_code)
    #adding the encoded data into database
    with open("database.txt", "a") as files:
        line = f"{encoded_name}, {score}, {time} \n"
        files.write(line)

ending(100, 24.7)

#OUTPUT
C:\Users\ASUS\PycharmProjects\pythonProject2\venv\Scripts\python.exe C:/Users/ASUS/PycharmProjects/pythonProject2/main.py
Please enter your username to record your score. 
>> Mary

Process finished with exit code 0

#In database.txt

Pdub, 100, 24.7 
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

#Testing if the function successfully finds, encodes to match the database and displays it 

def find(name):
    shift = 3
    #encoding the name to match the data in the database
    encoded_name = ''
    for i in range(len(name)):
        letter = name[i]
        letter_code = ord(letter)
        shifted_code = letter_code + shift
        if (shifted_code > 122 and letter.islower()) or (shifted_code > 90 and letter.isupper()):
            shifted_code -= 26
        encoded_name += chr(shifted_code)
    #finding the player in the database
    exist = False
    with open("database.txt", "r") as files:
        for player in files.readlines():
            name_stored, score_stored, time_stored = player.split(',')
            if name_stored == encoded_name:
                score = score_stored
                time = time_stored
                print(f"User found, you have {score} points and played for {time}.")
                exist = True
                break
    if exist == False:
        print("User does not exist, please try again.")

find("Mary")

#OUTPUT
C:\Users\ASUS\PycharmProjects\pythonProject2\venv\Scripts\python.exe C:/Users/ASUS/PycharmProjects/pythonProject2/main.py
User found, you have  100 points and played for  24.7
.

Process finished with exit code 0
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------

#Testing if the function successfully decodes all names and displays their scores and times

def display():
    with open("database.txt", "r") as files:
        for player in files.readlines():
            name_stored, score_stored, time_stored = player.split(',')
            name = name_stored
            score = score_stored
            time = time_stored
            shift = 3
            #decoding the names in the database to make it readable
            decoded_name = ''
            for i in range(len(name)):
                letter = name[i]
                letter_code = ord(letter)
                shifted_code = letter_code - shift
                if (letter.islower() and shifted_code < 96) or (letter.isupper() and shifted_code < 65):
                    shifted_code += 26
                decoded_name += chr(shifted_code)

            print(f"username = {decoded_name}, Score = {score}, Time = {time}")


display()

#OUTPUT

C:\Users\ASUS\PycharmProjects\pythonProject2\venv\Scripts\python.exe C:/Users/ASUS/PycharmProjects/pythonProject2/main.py
username = Mary, Score =  100, Time =  24.7

username = George, Score =  300, Time =  57.9 


Process finished with exit code 0
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
