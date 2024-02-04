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
import java.util.*;
public class Solution {
    public static List< Integer > majorityElement(int []v) {
        List<Integer> list=new ArrayList<Integer>(); // Creating Arraylist
        Arrays.sort(v); // Sorting
        int n = v.length;
        int mcount = 0; // Storing max count
        for(int i=0; i<n; i++){
            int count = 0; // Storing count for each element
            for(int j=i; j<n; j++){
                if (v[i]==v[j]){
                    count +=1;
                }
                else{
                    break;
                }
                mcount = Math.max(count, mcount); // Storing maximum count
            }
            // If max count is greater than 1 and element is not present in list
            if (mcount>Math.floor(n/3) && !list.contains(v[i])){
                list.add(v[i]);
                mcount=0;
            }else{
                mcount=0;
            }
        }
        Collections.sort(list);
        return list;
    }
}
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
import java.util.HashMap;

public class Solution {
    public static int getLongestZeroSumSubarrayLength(int []arr){
        // Brute Force
        // int mcount = 0;
        // int n = arr.length;
        // for(int i=0; i<n; i++){
        //     int count = 0;
        //     int sum = 0;
        //     for(int j=i; j<n; j++){
        //         sum += arr[j];
        //         count++;
        //         if (sum==0){
        //             mcount = Math.max(count, mcount);
        //         }
        //     }
        // }
        // return mcount;
     // Optimized
      HashMap<Integer, Integer> map = new HashMap<Integer, Integer>();
        int n = arr.length;
        int sum = 0;
        int max = 0;
        for(int i=0; i<n; i++){
            sum +=arr[i]; // Adding element to sum
            if (sum==0){ // if sum is equal to zero
                max=i+1;
            }
            else{
                if (map.get(sum)!=null){
                    max = Math.max(max, i-map.get(sum));
                }
                else{
                    map.put(sum, i);
                }
            }
        }
        return max;
    }
}
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
import java.util.*;
public class Solution {
    public static int[] findMissingRepeatingNumbers(int []a) {
        // int n = a.length;
        // int [] res = new int [2]; // For storing missing and repeat numbers
        // for(int i=1; i<=n; i++){ // loop for finding the missing and repeat numbers
        //      int count = 0; // Count occurance of each element
        //     for(int j=0; j<n; j++){ // Loop through array
        //         if (a[j]==i){
        //             count++; 
        //         }
        //     }
        //     if (count==2){ // For reapting numbers
        //         res[0] = i;
        //     }
        //     else if (count==0){ // For missing numbers
        //         res[1] = i;
        //     }
        // }

        // Optimized
        int n = a.length;
        int count = 0; // Count occurance of each element
        int [] res = new int[2];
        int [] hash = new int[n+1];
        for(int i=0; i<n; i++){
            hash[a[i]]++;
        }
        for(int i=1; i<=n; i++){
            if (hash[i] == 2){
                res[0] = i;
            }
            else if (hash[i]==0){
                res[1] = i;
            }
        }
        return res;
    }
}
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

