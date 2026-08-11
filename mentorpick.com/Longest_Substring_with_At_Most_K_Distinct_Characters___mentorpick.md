## [Longest Substring with At Most K Distinct Characters - mentorpick](https://mentorpick.com/code)

### Submitted: Aug 12, 2026, 12:11 AM

- **Language:** Unknown
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```
import java.util.*;
import java.io.*;

class BeingZero {
    public int solve(String s, int k) {
        int n = s.length(); 
        int start = 0; 
        int maxLen  =0; 
        HashMap<Character, Integer> map = new HashMap<>();
        for(int end = 0; end < n; end++) {
            char r = s.charAt(end);
            map.put(r, map.getOrDefault(r,0)+1); 
            while(map.size() > k) {
                char l = s.charAt(start); 
                map.put(l, map.get(l)-1); 
                if(map.get(l) == 0) {
                    map.remove(l); 
                 
                }
                start++; 
               
                
            }
             maxLen = Math.max(maxLen, end-start+1);
             
        }
        return maxLen; 
    }
}
```
