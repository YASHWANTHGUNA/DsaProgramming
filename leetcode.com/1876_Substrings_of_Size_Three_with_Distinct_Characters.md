## [1876. Substrings of Size Three with Distinct Characters](https://leetcode.com/problems/substrings-of-size-three-with-distinct-characters/submissions/2179899506)

### Submitted: Oct 23, 2026, 11:23 PM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```java
class Solution {
    public int countGoodSubstrings(String s) {
        int start = 0; 
        int count = 0; 
        HashMap<Character, Integer> map = new HashMap<>(); 
        for(int end = 0; end < s.length(); end++) {
            char ch = s.charAt(end); 
            map.put(ch, map.getOrDefault(ch, 0)+1); 
            if(end-start+1 > 3) {
                char left = s.charAt(start); 
                map.put(left, map.get(left)-1);
                if(map.get(left)==0) {
                    map.remove(left); 
                }
                start++;

            }
            if(end-start+1==3 && map.size()==3) {
                count++; 
            }

        }
        return count; 

        
    }
}
```
