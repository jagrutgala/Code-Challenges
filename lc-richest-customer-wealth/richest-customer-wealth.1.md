# Leet Code 1: richest-customer-wealth

## ts

```js
function maximumWealth(accounts: number[][]): number {
    let maxWealth = 0;
    for (let i = 0; i < accounts.length; i++) {
        const wealth = accounts[i].reduce((acc, x) => acc + x);
        maxWealth = wealth > maxWealth ? wealth : maxWealth;
    }
    return maxWealth;
};
```

Time: **54ms**(74.18%)

Memory: **51.53MB**(46.13%)


## cs

```cs
public class Solution {
    public int MaximumWealth(int[][] accounts) {
        int[] wealth = new int[accounts.Length];
        for (int i = 0; i < accounts.Length; i++) {
            wealth[i] = accounts[i].Aggregate((acc, x) => acc + x);
        }
        int maxWealth = wealth[0];
        for (int i = 0; i < wealth.Length; i++) {
            maxWealth = wealth[i] > maxWealth ? wealth[i]: maxWealth;
        }
        return maxWealth;
    }
}
```

Time: **62ms**(89.90%)

Memory: **41.00MB**(97.64%)

