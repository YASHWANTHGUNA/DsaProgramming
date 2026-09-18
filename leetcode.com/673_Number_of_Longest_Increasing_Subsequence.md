## [673. Number of Longest Increasing Subsequence](https://leetcode.com/problems/number-of-longest-increasing-subsequence/submissions/2146063317)

### Submitted: Sep 19, 2026, 12:12 AM

- **Language:** Java
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```java
class Solution {
    public int findNumberOfLIS(int[] nums) {
        int n = nums.length;
        int[] dp = new int[n]; 
        int[] count = new int[n]; 
        int maxLength = 0; 
        int answer = 0; 
        Arrays.fill(dp, 1);
        Arrays.fill(count,1); 
        for(int i = 0; i < n; i++) {
            for(int j = 0; j < i; j++) {
                if(nums[j] < nums[i]) {
                    if(dp[j] + 1 > dp[i])  {
                        dp[i] = dp[j] + 1; 
                        count[i] = count[j]; 
                    } else if(dp[j] + 1 == dp[i]) {
                        count[i] += count[j]; 
                    } 
                    
                    

                    
                     
                }
            }

            
           
        }
        for(int i = 0; i < n; i++) {
            if(dp[i] > maxLength ) {
                maxLength = dp[i]; 
                answer = count[i]; 
            } else if(dp[i] == maxLength) {
                answer += count[i]; 
            }
        }
        return answer; 
    }
}
```
