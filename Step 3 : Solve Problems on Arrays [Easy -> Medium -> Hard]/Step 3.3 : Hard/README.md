# [Print Pascal’s Triangle](https://www.codingninjas.com/studio/problems/print-pascal-s-triangle_6917910?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

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

# [Majority Element (>n/3)](https://www.codingninjas.com/studio/problems/majority-element_6915220?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
```

# [Three Sum](https://www.codingninjas.com/studio/problems/three-sum_6922132?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

# [Four Sum](https://www.codingninjas.com/studio/problems/4sum_5713771?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

# []()

### Solution
```Java
```
# []()

### Solution
```Java
```
# []()

### Solution
```Java
```
# []()

### Solution
```Java
```
# []()

### Solution
```Java
```
# []()

### Solution
```Java
```
# []()

### Solution
```Java
```
# []()

### Solution
```Java
```

