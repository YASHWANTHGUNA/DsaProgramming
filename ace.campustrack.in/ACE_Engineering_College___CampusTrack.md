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
