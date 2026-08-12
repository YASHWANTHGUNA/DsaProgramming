## [2958. Length of Longest Subarray With at Most K Frequency](https://leetcode.com/problems/length-of-longest-subarray-with-at-most-k-frequency/submissions/2104643945)

### Submitted: Aug 13, 2026, 12:06 AM

- **Language:** Java
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```java
class Solution {
    public int maxSubarrayLength(int[] nums, int k) {
    
        Map<Integer, Integer> freqMap = new HashMap<>();
        int left = 0;
        int maxLength = 0;
        
        for (int right = 0; right < nums.length; right++) {
            // Include the current element in the window
            freqMap.put(nums[right], freqMap.getOrDefault(nums[right], 0) + 1);
            
            // If the frequency exceeds k, shrink the window from the left
            while (freqMap.get(nums[right]) > k) {
                freqMap.put(nums[left], freqMap.get(nums[left]) - 1);
                left++;
            }
            
            // Update the maximum length found so far
            maxLength = Math.max(maxLength, right - left + 1);
        }
        
        return maxLength;


        
    }
}
```
