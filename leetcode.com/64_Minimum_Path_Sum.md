## [64. Minimum Path Sum](https://leetcode.com/problems/minimum-path-sum/submissions/2113111230)

### Submitted: Aug 19, 2026, 11:52 PM

- **Language:** Java
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```java
class Solution {
    public int minPathSum(int[][] grid) {
        int m = grid.length; 
        int n = grid[0].length; 
        int[][] dp = new int[m][n]; 
        dp[0][0] = grid[0][0]; 
        for(int j = 1; j < n; j++) {
            dp[0][j] = grid[0][j] + dp[0][j-1];
        } 
        for(int i = 1; i < m; i++) {
            dp[i][0] = grid[i][0] + dp[i-1][0]; 
        }
        for(int i = 1; i < m; i++) {
            for(int j = 1; j < n; j++) {
                dp[i][j] = grid[i][j] + Math.min(dp[i-1][j], dp[i][j-1]);
            }
        }
        return dp[m-1][n-1];
        
    }
}
```
