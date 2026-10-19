## [1838. Frequency of the Most Frequent Element](https://leetcode.com/problems/frequency-of-the-most-frequent-element/submissions/2176533263)

### Submitted: Oct 20, 2026, 12:33 AM

- **Language:** Java
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
class Solution {
    public int maxFrequency(int[] nums, int k) {
        Arrays.sort(nums); 
        int n = nums.length; 
        int maxFreq = 1; 
        long windowSum = 0; 
        long cost = 0; 
       
         
        int left = 0; 
        int right = 0; 
        while(right < n ) {
            windowSum += nums[right]; 
            cost = (long)nums[right] * (right-left+1) - windowSum; 
            while(cost  > k) {
                windowSum -= nums[left];
                left++; 
                cost = (long)nums[right] * (right-left+1) - windowSum; 
            }
            maxFreq = Math.max(maxFreq, right-left+1); 
            right++; 

        }
        return maxFreq; 
        
    }
}
```

---

### Submitted: Oct 20, 2026, 12:34 AM

- **Language:** Java
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
class Solution {
    public int maxFrequency(int[] nums, int k) {
        Arrays.sort(nums); 
        int n = nums.length; 
        int maxFreq = 1; 
        long windowSum = 0; 
        long cost = 0; 
       
         
        int left = 0; 
        int right = 0; 
        while(right < n ) {
            windowSum += nums[right]; 
            cost = (long)nums[right] * (right-left+1) - windowSum; 
            while(cost  > k) {
                windowSum -= nums[left];
                left++; 
                cost = (long)nums[right] * (right-left+1) - windowSum; 
            }
            maxFreq = Math.max(maxFreq, right-left+1); 
            right++; 

        }
        return maxFreq; 
        
    }
}
```
