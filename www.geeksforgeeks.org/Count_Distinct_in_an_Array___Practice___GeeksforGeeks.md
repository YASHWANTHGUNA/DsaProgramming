## [Count Distinct in an Array | Practice | GeeksforGeeks](https://www.geeksforgeeks.org/problems/find-distinct-elements--130928/1)

### Submitted: Aug 13, 2026, 03:04 PM

- **Language:** Unknown
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```
class Solution {
    static int countDistinct(int arr[]) {
        // code here
        HashSet<Integer> set = new HashSet<>();

        for (int i = 0; i < arr.length; i++) {
            set.add(arr[i]);
        }

        return set.size();
    }
}
```
