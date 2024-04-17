# Hacker Rank : array-left-rotation

## 2022-01-11

```py
#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'rotateLeft' function below.
#
# The function is expected to return an INTEGER_ARRAY.
# The function accepts following parameters:
#  1. INTEGER d
#  2. INTEGER_ARRAY arr
#

def rotateLeft(d, arr):
    # Write your code here
    rotated_arr= []
    length= len(arr)
    d= d% length
    # print(f"length: {length} d: {d}")
    if(d == 0): return arr
    for i in range(length):
        # print(f"i: {i} {(i+d)%length} arr[(i+d)%length]: {arr[(i+d)%length]}")
        rotated_arr.append(arr[(i+d)%length])

    return rotated_arr

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    first_multiple_input = input().rstrip().split()

    n = int(first_multiple_input[0])

    d = int(first_multiple_input[1])

    arr = list(map(int, input().rstrip().split()))

    result = rotateLeft(d, arr)

    fptr.write(' '.join(map(str, result)))
    fptr.write('\n')

    fptr.close()

```

Score: **22.00**(Accepted)
