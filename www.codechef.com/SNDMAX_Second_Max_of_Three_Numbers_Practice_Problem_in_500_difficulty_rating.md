## [SNDMAX. Second Max of Three Numbers Practice Problem in 500 difficulty rating](https://www.codechef.com/practice/course/basic-programming-concepts/DIFF500/problems/SNDMAX)

### Submitted: Aug 12, 2026, 12:30 AM

- **Language:** Unknown
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```
import java.util.*;
import java.lang.*;
import java.io.*;

class Codechef
{
	public static void main (String[] args) throws java.lang.Exception
	{
		Scanner sc = new Scanner(System.in);
		int N = sc.nextInt();
		for (int i = 0; i < N; i++) {
            int[] arr = new int[3];
            arr[0] = sc.nextInt();
            arr[1] = sc.nextInt();
            arr[2] = sc.nextInt();
            
            // Sort the array to arrange numbers in ascending order
            Arrays.sort(arr);
            
            // The second maximum will be at index 1
            System.out.println(arr[1]);
        }
		

	}
}
```
