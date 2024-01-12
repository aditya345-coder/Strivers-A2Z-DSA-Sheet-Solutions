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

# [Majority Element (>n/2 times)](https://www.codingninjas.com/studio/problems/majority-element_6783241?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution

```Java
class Solution {
    public int majorityElement(int[] nums) {
        int n = nums.length;
        Arrays.sort(nums); // Sorting array
        int mcount=0; // Maximum count
        for(int i=0; i<n; i++){
            int count=0; // count for each element
            for(int j=i; j<n; j++){
                if (nums[i]==nums[j]){
                    count+=1;
                }
                else{
                    break;
                }
                mcount = Math.max(count, mcount); // Getting maximum count
                
            }
            // Checking if maximum count is greater than n/2
            if (mcount>(n/2)){
                return nums[i];
            }
        }
        return mcount;
    }
}
```

# [Maximum Subarray Sum (Kadane's Algorithm)](https://www.codingninjas.com/studio/problems/maximum-subarray-sum_630526?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)

## Solution
```
import java.util.* ;
import java.io.*; 

public class Solution {
	public static long maxSubarraySum(int[] arr, int n) {
		long sum = 0;
		long max_sum = 0;
		for(int i=0; i<n; i++){
			sum = sum + arr[i];
			if (max_sum < sum){
				max_sum = sum;
			}
			if (sum < 0){
				sum = 0;
			}
		}
		return max_sum;
	}
}
```
# [Longest Subarray With Sum K (Print subarray with maximum subarray)](https://www.codingninjas.com/studio/problems/longest-subarray-with-sum-k_6682399?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTabValue=PROBLEM)

### Solution
```Java
```
