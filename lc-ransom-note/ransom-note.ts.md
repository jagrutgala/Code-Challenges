# Leet Code 1: ransom-note

## ts

```ts
const calculateFrequencyMap = (str: string) => {
    const charArr = str.split("");
    return charArr.reduce((acc, v) => {
        return {...acc, [v]: (acc[v] ?? 0) + 1};
    }, {});
}

function canConstruct(ransomNote: string, magazine: string): boolean {
    const ransomNoteMap = calculateFrequencyMap(ransomNote);
    const magazineMap = calculateFrequencyMap(magazine);
    console.log("Frequency Maps: ", {ransomNoteMap, magazineMap})

    const isSubset = Object.entries(ransomNoteMap).every((value) => {
        const [k,v] = value;
        return (k in magazineMap) && (magazineMap[k] >= v)
    });

    return isSubset;
};
```

Time: **239ms**(5.01%)

Memory: **60.53MB**(5.27%)
