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

# [Best time to buy and sell stock](https://www.codingninjas.com/studio/problems/best-time-to-buy-and-sell-stock_6194560?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
public class Solution {
    public static int bestTimeToBuyAndSellStock(int []prices) {
        int min = prices[0]; // Initilize minimum price
        int max_profit = 0; // Initilize a varaible which stores max profit
        for(int i=1; i<prices.length; i++){  
            if (prices[i]<min){ 
                min = prices[i]; // Taking minimum element
            }
		   // Check if current price subtracted from min price is greater than max profit
            else if (prices[i]-min>max_profit){ 
                max_profit = prices[i]-min;
            }
        }
        return max_profit;
    }
}
```

# [Alternate Numbers (Rearrange the array in alternating positive & negative)](https://www.codingninjas.com/studio/problems/alternate-numbers_6783445?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```
```

# [Next Greater Permutation](https://www.codingninjas.com/studio/problems/next-greater-permutation_6929564?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```
```

# [Superior Elements (Leaders in an Array problem)](https://www.codingninjas.com/studio/problems/superior-elements_6783446?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```
import java.util.*;
public class Solution {
    public static List< Integer > superiorElements(int []a) {
        List<Integer> list=new ArrayList<Integer>();  // Create a list
        int n = a.length;
        int largest=a[n-1]; // Take a variable which will store largest element
        for(int i=n-2; i>=0; i--){
            if (a[i]>largest){ // Largest element from right
                largest = a[i];
                list.add(largest);
            }
        }
        list.add(a[n-1]); // Add last element as it is always superior
        Collections.sort(list); // Sort list
        return list;
    }
}
```

# [Longest Consecutive Sequence in an Array (Longest Successive Elements)](https://www.codingninjas.com/studio/problems/longest-successive-elements_6811740?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
```

# [Zero Matrix](https://www.codingninjas.com/studio/problems/zero-matrix_1171153?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
```

# [Rotate The Matrix](https://www.codingninjas.com/studio/problems/rotate-the-matrix_6825090?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
```

# [Spiral Matrix](https://www.codingninjas.com/studio/problems/spiral-matrix_6922069?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
```

# [Count All Subarrays With Given Sum](https://www.codingninjas.com/studio/problems/subarray-sums-i_1467103?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution
```Java
```
