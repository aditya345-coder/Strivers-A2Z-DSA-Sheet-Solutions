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

# [Rotate array](https://www.codingninjas.com/studio/problems/rotate-array_1230543?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)

## Solution
```
import java.util.* ;
import java.io.*; 
class Solution {
	
	public static void main(String args[]) {
		Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int [] arr = new int[n];
        for (int i=0; i<n; i++)
        {
            arr[i]=sc.nextInt();
        }
        int k = sc.nextInt();
        Solution obj = new Solution();
        obj.rotate(arr,n,k);
      }
    void rotate(int arr[], int n, int k){
        for (int i=0; i<k; i++){
            int temp = arr[0];
            for (int j=0; j<n-1; j++){
                arr[j] = arr[j+1];
            }
            arr[n-1] = temp;
        }
        for (int a: arr){
            System.out.print(a+" ");
        }
    }        
}
```
# [Move Zero's to End](https://www.codingninjas.com/studio/problems/ninja-and-the-zero-s_6581958?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

## Solution
```
```
# [Linear Search](https://www.codingninjas.com/studio/problems/linear-search_6922070?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)

## Solution
```
import java.util.*;
public class Solution {
    public static int linearSearch(int n, int num, int []arr){
        for(int i=0; i<n; i++){
            if (arr[i]==num){
                return i;
            }
        }
        return -1;
    }
}
```

# [Missing Number](https://www.codingninjas.com/studio/problems/missing-number_6680467?utm_source=striver&utm_medium=website&utm_campaign=codestudio_a_zcourse&leftPanelTab=1)

## Solution
```
public class Solution {
    public static int missingNumber(int []a, int N) {
        int sum = 0;
        int arr_sum = 0;
        for (int i=1; i<N+1; i++){
            sum = sum + i;
        }
        for (int i=1; i<N+1; i++){
            arr_sum = arr_sum + a[i-1];
        }
        int missingNumber = sum - arr_sum;
        return missingNumber;
    }
}
```
