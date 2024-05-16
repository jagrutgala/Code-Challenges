# Leet Code : valid-anagram

## 23-Apr-2024 (1)

```js
const calculateFrequencyMap = (str: string): {[k : string]: number} => {
    const charArr = str.split("");
    return charArr.reduce((acc, v) => {
        return {...acc, [v]: (acc[v] ?? 0) + 1};
    }, {});
}

function isAnagram(s: string, t: string): boolean {
    const sMap = calculateFrequencyMap(s);

    for (let i = 0; i < t.length; i++) {
        const k = t[i];
        if (!(k in sMap)) {
            return false;
        }

        sMap[k] = sMap[k] - 1;
    }

    for (let v of Object.values(sMap)) {
        if (v != 0) {
            return false;
        }
    }
    return true;
};
```

Time: **140ms**(8.65%)

Memory: **58.84MB**(5.02%)

## 16-May-2024 (2)

```js
function isAnagram(s: string, t: string): boolean {
    if (s.length != t.length) {
        return false;
    }

    const sHashMap = s.split('').reduce((acc, v) => {
        acc[v] = (acc[v] ?? 0) + 1;
        return acc;
    }, {});

    for (const v of t) {
        if (!(v in sHashMap)) {
            return false;
        }
        sHashMap[v] = (sHashMap[v] ?? 0) - 1;
        if (sHashMap[v] < 0) {
            return false;
        }
    }
    return true;
};
```

Time: **65ms**(88.94%)

Memory: **53.29MB**(79.64%)
