## [Count Subarrays with Sum X - mentorpick](https://mentorpick.com/problemset/Subarray-Sums-II)

### Submitted: Aug 13, 2026, 02:28 PM

- **Language:** Unknown
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```
import java.util.*;
import java.io.*;

class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int T = sc.nextInt();
        while (T-- > 0) {
            int N = sc.nextInt();
            long X = sc.nextLong();
            long sum = 0;
            long count = 0;
            HashMap<Long, Integer> map = new HashMap<>();
            map.put(0L, 1);
            for (int i = 0; i < N; i++) {
                long value = sc.nextLong();
                sum += value;
                long needed = sum - X;
                if (map.containsKey(needed)) {
                    count += map.get(needed);
                }
                map.put(sum, map.getOrDefault(sum, 0) + 1);
            }
            System.out.println(count);
        }

        sc.close();
    }
}
```
