# Leet Code : first-unique-character-in-a-string

## 19-Apr-2024 (1)

```js
const calculateFrequencyMap = (str: string): {[k: string]: number} => {
    const charArr = str.split("");
    return charArr.reduce((acc, v) => {
        return {...acc, [v]: (acc[v] ?? 0) + 1};
    }, {});
}

function firstUniqChar(s: string): number {
    const charFrequency = calculateFrequencyMap(s);
    console.log(charFrequency);
    const nonRepeatingChars = Object.entries(charFrequency).filter(x => x[1] <= 1);
    if (nonRepeatingChars.length <= 0) {
        return -1;
    }
    console.log(nonRepeatingChars);
    const nonRepeatingIndex = nonRepeatingChars.map(x => s.indexOf(x[0]))
    let minIndex = s.length;
    for (let nri of nonRepeatingIndex) {
        if (nri < minIndex) {
            minIndex = nri;
        }
    }
    return minIndex;
};
```

Time: **556ms**(5.18%)

Memory: **65.55MB**(5.18%)


## 19-Apr-2024 (2)

```js
function firstUniqChar(str: string): number {
    const nonRepeatingMap = new Map();
    for (let i=0; i < str.length; i++) {
        const s = str[i];
        if (nonRepeatingMap.has(s)) {
            nonRepeatingMap.set(s, -1);
        }
        else {
            nonRepeatingMap.set(s, i);
        }
    }

    const nonRepeatingIndexes = Array.from(nonRepeatingMap.values()).filter(x => x >= 0);
    let nonRepeatingIndex = -1;
    if (nonRepeatingIndexes.length > 0) {
        nonRepeatingIndex = nonRepeatingIndexes[0];
    }
    return nonRepeatingIndex;
};
```

Time: **93ms**(65.36%)

Memory: **53.48MB**(90.71%)
