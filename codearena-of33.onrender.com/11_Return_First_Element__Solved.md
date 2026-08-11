## [11. Return First Element✓ Solved](https://codearena-of33.onrender.com/problems/11)

### Submitted: Aug 11, 2026, 08:17 PM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String input = sc.useDelimiter("\\A").next();
        input = input.replace("\\n", " ");

        Scanner data = new Scanner(input);

        int N = data.nextInt();

        int[] arr = new int[N];

        for (int i = 0; i < N; i++) {
            arr[i] = data.nextInt();
        }

        System.out.println(arr[0]);
    }
}
```
