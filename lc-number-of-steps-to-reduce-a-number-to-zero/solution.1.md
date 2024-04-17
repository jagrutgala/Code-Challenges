# Leet Code S1: number-of-steps-to-reduce-a-number-to-zero

## ts

```ts
function numberOfSteps(num: number): number {
    let steps = 0;
    while (num > 0) {
        if (num % 2 == 0) {
            num = num / 2;
        }
        else {
            num = num - 1;
        }
        steps++;
    };
    return steps;
};
```

Time: **49ms** (92.81%)

Memory: **51.45MB** (51.45%)


## cs

```cs
public class Solution {
    public int NumberOfSteps(int num) {
        int steps = 0;
        while (num > 0) {
            if (num % 2 == 0) {
                num = num / 2;
            }
            else {
                num = num - 1;
            }
            steps++;
        };
        return steps;
    }
}
```

Time: **31ms** (7.01%)

Memory: **26.80MB** (74.66%)
