# Leet Code : contains-duplicate

## 22-Apr-2024 (1)

```js
function containsDuplicate(nums: number[]): boolean {
    const numSet = new Set();
    for (let n of nums) {
        if (numSet.has(n)) {
            return true;
        }
        else {
            numSet.add(n);
        }
    }
    return false;
};
```

Time: **71ms**(87.57%)

Memory: **62.81MB**(31.99%)

