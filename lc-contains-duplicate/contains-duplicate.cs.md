# Leet Code : contains-duplicate

## 22-Apr-2024 (1)

```cs
public class Solution {
    public bool ContainsDuplicate(int[] nums) {
        HashSet<int> numSet = new HashSet<int>();
        foreach (int n in nums) {
            if (numSet.Contains(n)) {
                return true;
            }
            else {
                numSet.Add(n);
            }
        }
        return false;
    }
}
```

Time: **264ms**(66.41%)

Memory: **61.64MB**(53.61%)

