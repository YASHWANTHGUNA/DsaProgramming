## [Mean or Average of an Array | Practice | GeeksforGeeks](https://www.geeksforgeeks.org/problems/mean0021/1)

### Submitted: Aug 13, 2026, 12:58 PM

- **Language:** Unknown
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(1) (estimated)

```
class Solution {
    public static int findMean(int[] arr) {
        int sum = 0;

        for (int i = 0; i < arr.length; i++) {
            sum += arr[i];
        }

        return sum / arr.length;
        
    }
};
```
