# Hacker Rank : 2d-array

## 2022-01-11

```py
#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'hourglassSum' function below.
#
# The function is expected to return an INTEGER.
# The function accepts 2D_INTEGER_ARRAY arr as parameter.
#

def hourglassSum(arr):
    # Write your code here
    max_hourglass= None
    for i in range(1, 5):
        for j in range(1, 5):
            a= arr[i-1][j-1]
            a+= arr[i-1][j]
            a+= arr[i+1][j-1]
            a+= arr[i][j]
            a+= arr[i-1][j+1]
            a+= arr[i+1][j]
            a+= arr[i+1][j+1]
            print(a)
            if(max_hourglass == None):
                max_hourglass= a
            else:
                max_hourglass= max(max_hourglass, a)
    return max_hourglass



if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    arr = []

    for _ in range(6):
        arr.append(list(map(int, input().rstrip().split())))

    result = hourglassSum(arr)

    fptr.write(str(result) + '\n')

    fptr.close()

```

Score: **15.00**(Accepted)
