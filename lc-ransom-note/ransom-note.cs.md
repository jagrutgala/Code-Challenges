# Leet Code 1: ransom-note

## 1

```cs
public class Solution {
    public bool CanConstruct(string ransomNote, string magazine) {
        StringBuilder magazineSb = new StringBuilder(magazine);
        foreach (char c in ransomNote) {
            string magazineStr = magazineSb.ToString();
            if (!magazineStr.Contains(c)) {
                return false;
            }
            int index = magazineStr.IndexOf(c);
            magazineSb.Remove(index, 1);
            // Console.WriteLine(magazineSb.ToString());
        }
        return magazineSb.Length >= 0;
    }
}
```

Time: **65ms**(52.50%)

Memory: **122.66MB**(7.23%)


## 2

```cs
public class Solution {
    public bool CanConstruct(string ransomNote, string magazine) {
        foreach (char c in ransomNote) {
            if (!magazine.Contains(c)) {
                return false;
            }
            int index = magazine.IndexOf(c);
            magazine = magazine.Remove(index, 1);
            // Console.WriteLine(magazineSb.ToString());
        }
        return magazine.Length >= 0;
    }
}
```

Time: **57ms**(85.53%)

Memory: **122.80MB**(5.71%)
