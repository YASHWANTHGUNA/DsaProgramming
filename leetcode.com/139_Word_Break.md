## [139. Word Break](https://leetcode.com/problems/word-break/submissions/2117717805)

### Submitted: Aug 24, 2026, 12:01 AM

- **Language:** Java
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```java
class Solution {
    public boolean wordBreak(String s, List<String> wordDict) {
        int n = s.length(); 
        boolean[] dp = new boolean[n+1]; 
        dp[0] = true;
        for(int i = 1; i < n+1; i++) {
            for(int j = 0; j < i; j++) {
                if(dp[j] && wordDict.contains(s.substring(j,i))) {
                    dp[i] = true; 
                    // break;  
                }
            }
        }
        return dp[n];

        
    }
}
```
