# [Selection Sort](https://www.codingninjas.com/studio/problems/selection-sort_624469?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)

## Solution
```
public class Solution {
    public static void selectionSort(int[] arr) {
        
        for (int i=0; i<arr.length-1; i++){
            int min_index = i;
            // int j=i+1; 
            for (int j=i+1; j< arr.length; j++){
                if (arr[j]<arr[min_index]){
                    min_index = j;
                }

            }
            int temp = arr[i];
            arr[i] = arr[min_index];
            arr[min_index] = temp;
        }
    }
}
```
