## [1. Two Sum✓ Solved](https://codearena-of33.onrender.com/problems/1)

### Submitted: Aug 11, 2026, 01:35 AM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```java
// Java Solution
// Java Solution
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Read complete input
        String input = sc.useDelimiter("\\A").hasNext() ? sc.next() : "";

        // Convert literal "\n" into whitespace
        input = input.replace("\\n", " ");

        Scanner parser = new Scanner(input);

        if (!parser.hasNextInt()) return;

        int n = parser.nextInt();
        int target = parser.nextInt();

        int[] nums = new int[n];

        for (int i = 0; i < n; i++) {
            nums[i] = parser.nextInt();
        }

        HashMap<Integer, Integer> map = new HashMap<>();

        for (int i = 0; i < n; i++) {
            int complement = target - nums[i];

            if (map.containsKey(complement)) {
                System.out.println(map.get(complement) + " " + i);
                return;
            }

            map.put(nums[i], i);
        }
    }
}
```
