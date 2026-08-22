## [1685. Sum of Absolute Differences in a Sorted Array](https://leetcode.com/problems/sum-of-absolute-differences-in-a-sorted-array/submissions/2116446785)

### Submitted: Aug 22, 2026, 11:06 PM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```java
class Solution {
    public int[] getSumAbsoluteDifferences(int[] nums) {
        int n = nums.length; 
        int leftSum = 0; 
       
        int totalSum = 0; 
        int[] answer = new int[n]; 
        for(int i = 0; i < n; i++) {
            totalSum += nums[i]; 
        }
        for(int i = 0; i < n; i++) {
            int rightSum = totalSum - nums[i]- leftSum; 
            int leftCount = i; 
            int rightCount = n-i-1; 
            int  leftContribution  = nums[i] * leftCount - leftSum;
            

             int rightContribution = rightSum - nums[i] * rightCount;
             answer[i] = leftContribution + rightContribution; 
             leftSum += nums[i]; 

        }
        return answer; 
        
    }
}
```
