# Leet Code : two-sum

## 2024-04-21 (1)

```js
function twoSum(nums: number[], target: number): number[] {
    for (let i = 0; i < nums.length; i++) {
        const a = nums[i];
        for(let j = i + 1; j < nums.length; j++) {
            const b = nums[j];
            if ((a + b) == target) {
                return [i,j];
            }
        }
    }
};
```

Time: **92ms**(40.56%)

Memory: **52.17MB**(67.70%)


## 2024-04-21 (S)

```ts
function twoSum(nums: number[], target: number): number[] {
    const record: Record<number, number> = {}
    nums.forEach((num, i) => {
        record[num] = i;
    });

    for(let i = 0; i < nums.length; i++) {
        const complementary = target - nums[i];
        const complIndex = record[complementary];
        if (complIndex != null && complIndex !== i) return [i, complIndex]
    }
};
```

Time: **60ms**(79.96%)

Memory: **52.79MB**(36.04%)
