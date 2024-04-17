# Hacker Rank: day-of-the-programmer

## 1

```py
import datetime
# Complete the 'dayOfProgrammer' function below.
#
# The function is expected to return a STRING.
# The function accepts INTEGER year as parameter.

def is_leap_Julian(year):
    return year % 4 == 0
def is_leap_Gregorian(year):
    return year % 400 == 0 or (year % 4 == 0 and year % 100 != 0)


def dayOfProgrammer(year):
    # Write your code here
    # normal year 256th day = 13-09-yyyy
    date = datetime.date(year, 9, 13)
    days_to_add = 0
    if year < 1918 and is_leap_Julian(year): days_to_add -= 1
    elif year == 1918: days_to_add += 13
    elif year > 1918 and is_leap_Gregorian(year): days_to_add -= 1
    date = date + datetime.timedelta(days_to_add)
    return f"{date.day}.{date.month:02d}.{date.year}"


if __name__ == '__main__':
    year = int(input().strip())
    result = dayOfProgrammer(year)
    print(result)

```

Score: **15.0**
