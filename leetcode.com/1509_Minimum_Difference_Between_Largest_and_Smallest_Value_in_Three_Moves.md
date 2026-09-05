## [1509. Minimum Difference Between Largest and Smallest Value in Three Moves](https://leetcode.com/problems/minimum-difference-between-largest-and-smallest-value-in-three-moves/submissions/2131480470)

### Submitted: Sep 5, 2026, 01:36 PM

- **Language:** Java
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
class Solution {
    public int minDifference(int[] nums) {
        int n = nums.length; 
        Arrays.sort(nums);
        int answer = Integer.MAX_VALUE; 
        
        if(n <= 4) {
            return 0; 
        }
        for(int left = 0; left <= 3; left++) {
            for(int right = 3-left; right >= 0; right--) {
                int min = nums[left]; 
                int max = nums[n-1-right]; 
                int difference = max-min;
                answer = Math.min(answer, difference); 
               
            } 
            


        }
        return answer; 
        
    }
}
```
