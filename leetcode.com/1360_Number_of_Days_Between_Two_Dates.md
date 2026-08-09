## [1360. Number of Days Between Two Dates](https://leetcode.com/problems/number-of-days-between-two-dates)

### Submitted: Aug 9, 2026, 09:13 PM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
class Solution {
    public int daysBetweenDates(String date1, String date2) {
        return Math.abs(countDays(date1) - countDays(date2));
    }
    
    // Helper function to count days from 1971-01-01 to the given date
    private int countDays(String date) {
        String[] parts = date.split("-");
        int year = Integer.parseInt(parts[0]);
        int month = Integer.parseInt(parts[1]);
        int day = Integer.parseInt(parts[2]);
        
        int totalDays = 0;
        
        // 1. Add days for all previous years starting from 1971
        for (int y = 1971; y < year; y++) {
            totalDays += isLeapYear(y) ? 366 : 365;
        }
        
        // 2. Add days for completed months in the current year
        int[] daysInMonths = { 0, 31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31 };
        for (int m = 1; m < month; m++) {
            if (m == 2 && isLeapYear(year)) {
                totalDays += 29;
            } else {
                totalDays += daysInMonths[m];
            }
        }
        
        // 3. Add days of the current month
        totalDays += day;
        
        return totalDays;
    }
    
    private boolean isLeapYear(int year) {
        return (year % 4 == 0 && year % 100 != 0) || (year % 400 == 0);
    }
}
```
