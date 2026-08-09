## [Is Two Sum Exist? - mentorpick](https://mentorpick.com/code)

### Submitted: Aug 9, 2026, 11:54 PM

- **Language:** Unknown
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```
class BeingZero {
    public boolean solve(int[] a, int n, int k) {
       HashSet<Integer> set = new HashSet<>(); 
        for(int num : a) {
            int comp = k - num; 
            if(set.contains(comp) && comp!=num) {
                return true;
            }
            set.add(num);
        }
         return false; 
    }
}
```
