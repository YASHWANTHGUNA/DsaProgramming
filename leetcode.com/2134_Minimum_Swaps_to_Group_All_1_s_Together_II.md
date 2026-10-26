## [2134. Minimum Swaps to Group All 1's Together II](https://leetcode.com/problems/minimum-swaps-to-group-all-1s-together-ii/submissions/2182492395)

### Submitted: Oct 26, 2026, 11:30 PM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
class Solution {
    public int minSwaps(int[] nums) {
        int n =nums.length;
        int totalOnes = 0; 
        for(int i = 0; i < n; i++) {
            if(nums[i] == 1) {
                totalOnes++; 
            }
        }
        if(totalOnes ==  0 || totalOnes == n) {
            return 0; 
        }
        int currentZeroes = 0; 
        for(int i = 0; i < totalOnes; i++) {
            if(nums[i] == 0) {
                currentZeroes++; 
            }
        }
        int minSwaps = currentZeroes; 
        for(int i = 1; i < n; i++) {
            if(nums[i-1]==0) {
                currentZeroes--; 
            }
            int incomingIdx = (i+totalOnes-1)%n; 
            if(nums[incomingIdx]==0) {
                currentZeroes++; 
            }
            minSwaps = Math.min(minSwaps, currentZeroes);
        }
        return minSwaps; 

    }
}
```
