## [Minimum Operations | Practice | GeeksforGeeks](https://www.geeksforgeeks.org/problems/find-optimum-operation4504/1)

### Submitted: Aug 9, 2026, 11:32 PM

- **Language:** Unknown
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(1) (estimated)

```
class Solution {
    public int minOperation(int n) {
        int operations = 0;
        
        while (n > 0) {
            if (n % 2 == 0) {
                n /= 2; // Reverse of doubling
            } else {
                n -= 1; // Reverse of adding 1
            }
            operations++;
        }
        
        return operations;
    }
}
```
