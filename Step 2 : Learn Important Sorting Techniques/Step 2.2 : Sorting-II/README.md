# 1. [Merge Sort](https://www.codingninjas.com/studio/problems/merge-sort_5846?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)
## Solution:

```Java
public class Solution {
    static void merge(int arr[], int l, int m, int r){
        int n1=m-l+1,n2=r-m;
        int [] L = new int[n1];
        int [] M = new int[n2];

        for(int i=0;i<n1;i++){
            L[i]=arr[l+i];
        }
        for(int j=0;j<n2;j++){
            M[j]=arr[m+j+1];
        }

        int i=0,j=0,k=l;
        while(i<n1 && j<n2){
            if (L[i]<=M[j]){
                arr[k]=L[i];
                i++;
            }
            else{
                arr[k]=M[j];
                j++;
            }
            k++;
        }

        while(i<n1){
            arr[k]=L[i];
            i++;
            k++;
        }

        while(j<n2){
            arr[k]=M[j];
            j++;
            k++;
        }
    }
    public static void mergeSort(int[] arr, int l, int r){
        if (l<r){
            int m=(l+r)/2;
            mergeSort(arr,l,m);
            mergeSort(arr, m+1, r);
            merge(arr, l, m, r);
        }
    }
}
```
