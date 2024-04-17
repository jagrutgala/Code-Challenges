# Leet Code 2 : richest-customer-wealth

## ts

```js
function maximumWealth(accounts: number[][]): number {
     return Math.max(...accounts.map(holder => holder.reduce((a, b)=> a+b)));
};
```

Time: **45ms**(97.01%)

Memory: **51.44MB**(62.22%)


## cs

```cs
public class Solution {
    public int MaximumWealth(int[][] accounts) {
        int maxWealth = 0;
        for (int i = 0; i < accounts.Length; i++) {
            int wealth = accounts[i].Aggregate((acc, x) => acc + x);
            maxWealth = wealth > maxWealth ? wealth: maxWealth;
        }
        return maxWealth;
    }
}
```

Time: **63ms**(86.65%)

Memory: **40.95MB**(97.64%)
