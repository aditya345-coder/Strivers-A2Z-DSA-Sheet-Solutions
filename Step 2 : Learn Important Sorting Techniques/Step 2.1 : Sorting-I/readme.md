# 1. [Selection Sort](https://www.codingninjas.com/studio/problems/selection-sort_624469?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)

## Java Solution
```Java
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
# 2. [Bubble Sort](https://www.codingninjas.com/studio/problems/bubble-sort_624380?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=1)

## Java Solution
```Java
public class Solution {
    public static void bubbleSort(int[] arr, int n) {
        for(int i=0; i<arr.length-1; i++){
            boolean swapped = false;
            for(int j=0; j<arr.length-i-1; j++){
                if (arr[j]>arr[j+1]){
                    int temp = arr[j];
                    arr[j] = arr[j+1];
                    arr[j+1] = temp;
                    
                    swapped = true;
                }
                
            }
            if (!swapped){
                break;
            }
        }
    }
}
```
## Python Solution
```Python
from typing import List

def bubbleSort(arr: List[int], n: int):
    for i in range(len(arr)-1):
        swapped = False
        for j in range(len(arr)-i-1):
            if (arr[j]>arr[j+1]):
                temp = arr[j]
                arr[j] = arr[j+1]
                arr[j+1] = temp

                swapped = True
        if (swapped!=True):
            break
```
# 3. [Recursive Insertion sort](https://www.codingninjas.com/studio/problems/insertion-sort_624381?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

## Java Solution
```Java
public class Solution {
    public static void insertionSort(int[] arr, int size) {
        for (int i=1; i<size; i++){
            int j = i-1;
            int key = arr[i];
            while(j>=0 && arr[j]> key){
                arr[j+1] = arr[j];
                j--;
            }
            arr[j+1] = key;
        }
    }
}
```
