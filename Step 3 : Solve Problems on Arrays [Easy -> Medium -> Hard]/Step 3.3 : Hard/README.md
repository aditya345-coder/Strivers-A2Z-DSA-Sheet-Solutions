# 1. [Print Pascal’s Triangle](https://www.codingninjas.com/studio/problems/print-pascal-s-triangle_6917910?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
import java.util.*;
public class Solution {
    public static int[][] pascalTriangle(int N) {
        int [][] a = new int [N][]; // Declaring 2D array
        for(int i=0; i<N; i++){
            int [] b = new int [i+1]; // Creating temp arrat
            for(int j=0; j<=i; j++){
                if (j==0 || j==i){
                    b[j] = 1; \\ Assign 1 to every starting and ending 
                }else{
                    b[j] = a[i-1][j-1] + a[i-1][j];  // Otherwise sum of previous element
                }
            }
            a[i] = b; // Adding temp array to 2D array
        }
        return a;
    }
}
```

# 2. [Majority Element (>n/3)](https://www.codingninjas.com/studio/problems/majority-element_6915220?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
```

# 3. [Three Sum](https://www.codingninjas.com/studio/problems/three-sum_6922132?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
```

# 4. [Four Sum](https://www.codingninjas.com/studio/problems/4sum_5713771?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
```

# 5. [Longest Subarray With Zero Sum](https://www.codingninjas.com/studio/problems/longest-subarray-with-zero-sum_6783450?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
```

# 6. [Subarrays with XOR ‘K’](https://www.codingninjas.com/studio/problems/subarrays-with-xor-k_6826258?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
```
# 7. [Merge All Overlapping Intervals](https://www.codingninjas.com/studio/problems/merge-all-overlapping-intervals_6783452?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
```
# 8. [Merge Two Sorted Arrays Without Extra Space](https://www.codingninjas.com/studio/problems/merge-two-sorted-arrays-without-extra-space_6898839?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
```
# 9. [Missing And Repeating Numbers](https://www.codingninjas.com/studio/problems/missing-and-repeating-numbers_6828164?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
```
# 10. [Number of Inversions](https://www.codingninjas.com/studio/problems/number-of-inversions_6840276?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
```
# 11. [Team Contest](https://www.codingninjas.com/studio/problems/team-contest_6840309?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
```
# 12. [Subarray With Maximum Product](https://www.codingninjas.com/studio/problems/subarray-with-maximum-product_6890008?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
```

