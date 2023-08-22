# [Reading](https://www.codingninjas.com/studio/problems/reading_6845742?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)

## Solution
```
public class Solution {
    public static String read(int n, int []book, int target){
        for (int i=0; i<n; i++){
            for (int j=0; j<n; j++){
                if (book[i]+book[j] == target){
                    return "YES";
                }
            }
        }
        return "NO";
    }
}
```
# [Sort An Array of 0s, 1s and 2s](https://www.codingninjas.com/studio/problems/sort-an-array-of-0s-1s-and-2s_892977?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)

## Solution
```
import java.util.*;
import java.io.*; 
public class Solution {
    public static void sortArray(ArrayList<Integer> arr, int n) {
        int low =0, mid = 0, high = n-1;
        while (mid<=high){
            if (arr.get(mid)==0){
                Collections.swap(arr, low, mid);
                mid++;
                low++;
            }
            else if (arr.get(mid) == 1){
                mid++;
            }
            else{
                Collections.swap(arr, high, mid);
                high--;
            }
        }
    }
}

```
