## [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/submissions/2105122029)

### Submitted: Aug 13, 2026, 12:48 PM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
class Solution {
    public int maxArea(int[] height) {
        int n = height.length; 
        int left = 0; 
        int right = n-1;
        int maxArea = 0; 
        while(left < right) {
            int width = right-left; 
            int h = Math.min(height[left], height[right]); 
            int area = h * width; 
            maxArea = Math.max(maxArea, area); 
            if(height[left] <= height[right]) {
                left++; 
            } else {
                right--; 
            }

        }
         return maxArea; 

        
    }
}
```
