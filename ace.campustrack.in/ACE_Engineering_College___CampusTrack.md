## [ACE Engineering College - CampusTrack](https://ace.campustrack.in/question/check-if-number-is-negative)

### Submitted: Aug 9, 2026, 11:50 PM

- **Language:** Java
- **Time Complexity:** O(1) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;

//===== Declare Imports here if required =====


public class Main {

    //===== Declare Global Variables / Functions here if required =====


    public static void main(String[] args) throws Exception {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine());

        //===== Declare Local Variables / Functions here if required =====


        //===== Write Your Logic Here =====
                    if(n < 0) {
                        System.out.println("True");
                    } else {
                        System.out.println("False");
                    }

    }
}
```

---

### Submitted: Aug 11, 2026, 11:55 PM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

//===== Declare Imports here if required =====


public class Main {

    //===== Declare Global Variables / Functions here if required =====


    public static void main(String[] args) throws Exception {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

        int n = Integer.parseInt(br.readLine());
        StringTokenizer st = new StringTokenizer(br.readLine());

        //===== Declare Local Variables / Functions here if required =====


        int[] arr = new int[n];

        for (int i = 0; i < n; i++) {
            arr[i] = Integer.parseInt(st.nextToken());
        }

        //===== Write Your Logic Here =====
        int sum = 0;
        for(int i = 0; i < n; i++) {
            sum += arr[i];
        } 
        System.out.println(sum);

    }
}
```
