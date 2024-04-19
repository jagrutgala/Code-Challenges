# Leet Code : first-unique-character-in-a-string

## 19-Apr-2024 (1)

```cs
public class Solution {
    public int FirstUniqChar(string str) {
        Dictionary<char, int> nonRepeatingMap = new Dictionary<char, int>();
        for (int i=0; i < str.Length; i++) {
            char s = str[i];
            if (nonRepeatingMap.ContainsKey(s)) {
                nonRepeatingMap[s] = -1;
            }
            else {
                nonRepeatingMap[s] = i;
            }
        }

        int minNonRepeatingIndex = str.Length + 1;
        foreach (int s in nonRepeatingMap.Values) {
            if (s == -1) {
                continue;
            }
            if (s < minNonRepeatingIndex) {
                minNonRepeatingIndex = s;
            }
        }

        if (minNonRepeatingIndex < str.Length) {
            return minNonRepeatingIndex;
        }
        return -1;
    }
}
```

Time: **57ms**(74.69%)

Memory: **47.67MB**(58.16%)
