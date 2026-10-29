## [3206. Alternating Groups I](https://leetcode.com/problems/alternating-groups-i/submissions/2184819372)

### Submitted: Oct 29, 2026, 08:47 PM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
class Solution {
    public int numberOfAlternatingGroups(int[] colors) {
        int count  =0; 
        int n = colors.length; 
        for(int i = 0; i < n; i++) {
            int left = colors[(i-1+n)%n];
            int middle = colors[i];
            int right = colors[(i+1)%n];
            if(middle != left && middle != right) {
                count++; 
            }
        }
        return count; 
    }
}
```
