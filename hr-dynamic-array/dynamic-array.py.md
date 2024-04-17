# Hacker Rank : dynamic-array

## 2022-01-11

```py
#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'dynamicArray' function below.
#
# The function is expected to return an INTEGER_ARRAY.
# The function accepts following parameters:
#  1. INTEGER n
#  2. 2D_INTEGER_ARRAY queries
#

def dynamicArray(n, queries):
    # Write your code here
    arr2d= [list() for _ in range(n)]
    answers_arr= []
    last_answer= 0
    # x= (x^last_answer)% n
    for k, q in enumerate(queries):
        idx= (q[1]^ last_answer)% n
        if(q[0] == 1):
            arr2d[idx].append(q[2])
        else:
            last_answer= arr2d[idx][q[2]% len(arr2d[idx])]
            answers_arr.append(last_answer)

    return answers_arr

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    first_multiple_input = input().rstrip().split()

    n = int(first_multiple_input[0])

    q = int(first_multiple_input[1])

    queries = []

    for _ in range(q):
        queries.append(list(map(int, input().rstrip().split())))

    result = dynamicArray(n, queries)

    fptr.write('\n'.join(map(str, result)))
    fptr.write('\n')

    fptr.close()

```

Score: **15.00**(Accepted)
