## [1961. Check If String Is a Prefix of Array](https://leetcode.com/problems/check-if-string-is-a-prefix-of-array/submissions/2105241844)

### Submitted: Aug 13, 2026, 02:59 PM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
class Solution {
    public boolean isPrefixString(String s, String[] words) {
        String temp = "";

        for (int i = 0; i < words.length; i++) {
            temp = temp + words[i];

            if (temp.equals(s)) {
                return true;
            }

            
            if (temp.length() > s.length()) {
                return false;
            }
        }

        return false;

        
    }
}
```
