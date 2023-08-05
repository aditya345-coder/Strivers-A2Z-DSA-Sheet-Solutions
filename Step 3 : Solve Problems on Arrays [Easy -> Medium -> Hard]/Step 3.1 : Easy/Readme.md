# [Largest Element in the Array ](https://www.codingninjas.com/studio/problems/largest-element-in-the-array-largest-element-in-the-array_5026279?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)

## Solution
```
import java.util.* ;
import java.io.*; 

public class Solution {
    static int largestElement(int[] arr, int n) {
        int max = arr[0];
        for(int i=1; i<n; i++){
            if (max<arr[i]){
                max = arr[i];
            }
        }
        return max;
    }
}
```

# [Ninja And The Second Order Elements ](https://www.codingninjas.com/studio/problems/ninja-and-the-second-order-elements_6581960?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=1)

## Solution
```
public class Solution {
    public static int[] getSecondOrderElements(int n, int []a) {
        for (int i=1; i<n; i++){
            int j = i-1;
            int key = a[i];
            while(j>=0 && a[j]>key){
                a[j+1] = a[j];
                j--;
            }
            a[j+1] = key;
        }
        int [] arr = {a[n-2],a[1]};
        return arr;
    }
}
```
# [Ninja And The Sorted Check](https://www.codingninjas.com/studio/problems/ninja-and-the-sorted-check_6581957?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)

## Solution
```
import java.util.*;
public class Solution {
    public static int isSorted(int n, int []a) {
        int b[] = new int[a.length];
        for (int i = 0; i < a.length; i++)
            b[i] = a[i];
        
        Arrays.sort(b);
        if (Arrays.equals(a,b)){
            return 1;
        }
        return 0;     
    }
}
```
# [Left Rotate an Array by One](https://www.codingninjas.com/studio/problems/left-rotate-an-array-by-one_5026278?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)

## Solution
```
import java.util.* ;
import java.io.*; 

public class Solution {
    static int[] rotateArray(int[] arr, int n) {
        int temp = arr[0];
        for (int i=1; i<n; i++){
            arr[i-1] = arr[i];
        }
        arr[n-1] = temp;
        return arr;
    }
}
```
