## [1323. Maximum 69 Number](https://leetcode.com/problems/maximum-69-number/submissions/2106943228)

### Submitted: Aug 14, 2026, 11:49 PM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
class Solution {
    public int maximum69Number (int num) {
        char[] arr = String.valueOf(num).toCharArray();

        for (int i = 0; i < arr.length; i++) {
            if (arr[i] == '6') {
                arr[i] = '9';
                break;
            }
        }

        return Integer.parseInt(new String(arr));
        
    }
}
```
