# Leet Code S2: number-of-steps-to-reduce-a-number-to-zero

## ts

```ts
function numberOfSteps(num: number): number {
    let steps = 0;
    while (num > 0) {
        if (num == 1) {
            num -= 1;
            steps++;
        }
        else if (num % 2 != 0) {
            num = (num - 1) / 2;
            steps += 2;
        }
        else {
            num = num / 2;
            steps++;
        }
    };
    return steps;
};
```

Time: **44ms** (98.97%)

Memory: **51.32MB** (38.19%)


## cs

```cs
public class Solution {
    public int NumberOfSteps(int num) {
        int steps = 0;
        while (num > 0) {
            if (num == 1) {
                num = num - 1;
                steps++;
            }
            else if (num % 2 != 0) {
                num = (num - 1) / 2;
                steps += 2;
            }
            else {
                num = num / 2;
                steps++;
            }
        };
        return steps;
    }
}
```

Time: **14ms** (95.48%)

Memory: **26.70MB** (74.66%)

