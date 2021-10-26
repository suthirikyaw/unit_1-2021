```.py
#Name of file is Date.py
def weekday():
    from datetime import date

    day = date.today().weekday()

    if day == 0:
        return("Monday")
    if day == 1:
        return("Tuesday")
    if day == 2:
        return("Wednesday")
    if day == 3:
        return("Thursday")
    if day == 4:
        return("Friday")
    if day == 5:
        return("Saturday")
    if day == 6:
        return("Sunday")

def date():
    from datetime import date

    date = str(date.today())
    date1 = date[8:10]
    return date1
