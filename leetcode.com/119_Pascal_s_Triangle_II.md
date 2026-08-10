## [119. Pascal's Triangle II](https://leetcode.com/problems/pascals-triangle-ii/submissions/2102035327)

### Submitted: Aug 11, 2026, 01:47 AM

- **Language:** Java
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```java
class Solution {
    public List<Integer> getRow(int rowIndex) {
        List<Integer> row = new ArrayList<>();
        
        // Initialize the first element as 1
        for (int i = 0; i <= rowIndex; i++) {
            row.add(1);
        }
        
        // Compute values from row 2 up to rowIndex
        for (int i = 2; i <= rowIndex; i++) {
            // Update backwards to use previous row's values safely
            for (int j = i - 1; j > 0; j--) {
                row.set(j, row.get(j) + row.get(j - 1));
            }
        }
        
        return row;
    }
}
```
