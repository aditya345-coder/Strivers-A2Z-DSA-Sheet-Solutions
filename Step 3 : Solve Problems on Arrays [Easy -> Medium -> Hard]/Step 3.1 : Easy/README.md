# 1. [Largest Element in the Array ](https://www.geeksforgeeks.org/problems/largest-element-in-array4009/0?utm_source=youtube&utm_medium=collab_striver_ytdescription&utm_campaign=largest-element-in-array)

## Java Solution
```Java
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
// Time Complexity: O(n), Space Complexity: O(1)
```

## Python Solution
```Python
from typing import List

class Solution:
    def largest(self, arr : List[int]) -> int:
        maximum=0
        for i in range(len(arr)):
            if (maximum<arr[i]):
                maximum=arr[i]
        return maximum

# Time Complexity: O(n), Space Complexity: O(1)
```
# 2. [Ninja And The Second Order Elements ](https://www.geeksforgeeks.org/problems/second-largest3735/1?utm_source=youtube&utm_medium=collab_striver_ytdescription&utm_campaign=second-largest)

## Java Solution
```Java
public class Solution {
    public static int[] getSecondOrderElements(int n, int []a) {
	// Insertion Sort
        for (int i=1; i<n; i++){
            int j = i-1;
            int key = a[i];
            while(j>=0 && a[j]>key){
                a[j+1] = a[j];
                j--;
            }
            a[j+1] = key;
        }
	// storing largest and smallest element
        int [] arr = {a[n-2],a[1]};
        return arr;
    }
}
// Time Complexity: O(n^2), Space Complexity: O(1)
```

## Java Solution (Method 2)
```Java
import java.util.*;
public class Solution {
    public static int[] getSecondOrderElements(int n, int []a) {
        // Initializing the driver variables.
        int small = Integer.MAX_VALUE, secondSmall = Integer.MAX_VALUE;
        int large = Integer.MIN_VALUE, secondLarge = Integer.MIN_VALUE;

        // Iterating over an array and calculating the smaller and larger numbers.
        for (int i = 0; i < n; i++) {
            small = Math.min(small, a[i]);
            large = Math.max(large, a[i]);
        }

        // Iterating again and updating the second order numbers.
        for (int i = 0; i < n; i++) {
            if (a[i] < secondSmall && a[i] != small) {
                secondSmall = a[i];
            }
            if (a[i] > secondLarge && a[i] != large) {
                secondLarge = a[i];
            }
        }
        return new int[]{secondLarge, secondSmall};
    }
}
// Time complexity: O(N), Space complexity: O(1)
```

## Python Solution
```Python
class Solution:
    def getSecondLargest(self, arr):
        largest=max(arr)  # O(n)
        second_largest = -1
        for i in range(len(arr)):  # O(n)
            if (second_largest<arr[i] and arr[i]<largest):
                second_largest=arr[i]
        return second_largest

# Time Complexity: O(n), Space Complexity: O(1)
```

# 3. [Ninja And The Sorted Check](https://leetcode.com/problems/check-if-array-is-sorted-and-rotated/description/)

## Java Solution - ([Coding Ninja](https://www.codingninjas.com/studio/problems/ninja-and-the-sorted-check_6581957?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)
)
```Java
import java.util.*;
public class Solution {
    public static int isSorted(int n, int []a) {
        int b[] = new int[a.length];
        for (int i = 0; i < a.length; i++)
            b[i] = a[i];
        
        Arrays.sort(b); // Tim Sort algorithm
        if (Arrays.equals(a,b)){
            return 1;
        }
        return 0;     
    }
}
// Time Complexity: O(nlogn), Space Complexity: O(1)
```

## Python
```Python
```
# 4. [Remove Duplicates from Sorted Array]

## Java Solution - [Coding Ninja](https://www.codingninjas.com/studio/problems/remove-duplicates-from-sorted-array_1102307?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTabValue=PROBLEM)
```Java
import java.util.ArrayList;

public class Solution {
	public static int removeDuplicates(ArrayList<Integer> arr,int n) {
		// first pointer
		int i=0; 
		// Second pointer
		for(int j=1; j<n; j++){
			// if not duplicates increment first pointer and check again
			 if (!arr.get(j).equals(arr.get(j - 1))) { // use .equals() for List
                arr.set(i++, arr.get(j));
            }
		}
		return i+1;
	}
}
```

## Python Solution
```Python
def removeDuplicates(arr,n):
    return len(set(arr))
```

## Alternate Solution
```Python
class Solution:
    def removeDuplicates(self, nums: List[int]) -> int:
        new_nums=[]
        for ele in nums:
            if (ele not in new_nums):
                new_nums.append(ele)
        
        for i in range(len(new_nums)):
            nums[i]=new_nums[i]

        return len(new_nums)

# Time Complexity: O(n) Space Complexity: O()
```

## Alternate Solution:
```Python
class Solution:
    def removeDuplicates(self, nums: List[int]) -> int:
        writer=0
        for reader in range(len(nums)):
            if (nums[reader]!=nums[writer]):
                writer+=1
            nums[writer]=nums[reader]
        
        return writer+1

Time Complexity: O(n)  Space Complexity: O(1)
```

# 5. [Left Rotate an Array by One]

## Java Solution - [Coding Ninja](https://www.codingninjas.com/studio/problems/left-rotate-an-array-by-one_5026278?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)
```Java
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
// Time Complexity: O(n), Space Complexity: O(1)
```

## Python
```Python
```

# 6. [Rotate array]

## Java Solution - [Coding Ninja](https://www.codingninjas.com/studio/problems/rotate-array_1230543?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)
```Java
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
// Time Complexity: O(n*k), Space Complexity: O(n)
```

## Python
```Python
```

# 7. [Move Zero's to End]

## Java Solution - [Coding Ninja](https://www.codingninjas.com/studio/problems/ninja-and-the-zero-s_6581958?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)
```Java
public class Solution {
    public static int[] moveZeros(int n, int []a) {
	int count=0;
	int [] arr = new int[n];
	int j=0;
	for(int i=0; i<n; i++){
	    if(a[i]!=0){
		arr[j]=a[i];
		j++;
	    }
        } 
	return arr;
}
// Time Complexity: O(n), Space Complexity: O(n)
```

## Alternate Solution:
```Java
class Solution {
    public void moveZeroes(int[] nums) {
       int temp = 0;
       for(int i=0; i<nums.length; i++){
            for(int j=i+1; j<nums.length; j++){
                if (nums[j]!=0 && nums[i]==0){
                    nums[i]=nums[j];
                    nums[j]=0;
                    break;
                }
            }
       }
    }
}
// Time Complexity: O(n^2), Space Complexity: O(1)
```

## Alternate Solution:
```Java
// 2 Pointer Approach
class Solution {
    public void moveZeroes(int[] nums) {
       int j = 0;
       for(int i=0; i<nums.length; i++){
            if (nums[i]!=0){
                int temp=nums[i];
                nums[i] = nums[j];
                nums[j] = temp;
                j++;
            }
       }
    }
}
// Time Complexity: O(n), Space Complexity: O(1)
```

## Python Solution
```Python
class Solution:
    def moveZeroes(self, nums: List[int]) -> None:
        """
        Do not return anything, modify nums in-place instead.
        """
        new_nums=[0]*len(nums)
        j=0
        for i in range(len(nums)):
            if nums[i]!=0:
                n=nums[i]
                new_nums[j]=n
                j+=1
        
        for i in range(len(new_nums)):
            nums[i]=new_nums[i]

# Time Complexity: O(n), Space Complexity: O(n)
```
## Python Solution
```Python
def moveZeros(n: int,  a: [int]) -> [int]:
    ln = a.count(0)
    for i in range(ln):
        a.remove(0)
        a.append(0)
    return a

# Time Complexity: O(n), Space Complexity: O(1)
```

## Python
```Python
class Solution:
    def moveZeroes(self, nums: List[int]) -> None:
        """
        Do not return anything, modify nums in-place instead.
        """
        # 2 Pointer approach
        left=0
        for right in range(len(nums)):
            if (nums[right]!=0):
                nums[left], nums[right]=nums[right], nums[left]
                left+=1

# Time Complexity: O(n), Space Complexity: O(1)
```

# 8. [Linear Search]

## Java Solution - [Coding Ninja](https://www.codingninjas.com/studio/problems/linear-search_6922070?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)
```Java
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
// Time Complexity: O(n), Space Complexity: O(1)
```

## Python
```Python
```

# 9. [Merge 2 Sorted Array]

## Java Solution - [Coding Ninja](https://www.codingninjas.com/studio/problems/sorted-array_6613259?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)
```Java
import java.util.*;
public class Solution {
    public static List< Integer > sortedArray(int []a, int []b) {
        List<Integer> uarr=new ArrayList<Integer>(); 
        int i=0, j=0; // Initilize 2 pointers
        while(i<a.length && j<b.length){ // Loop until one of pointer exceeds the length
			// If element of a is less and equal to element of b
			if (a[i]<=b[j]){
                if(uarr.size()==0 || uarr.get(uarr.size()-1)!=a[i]){
                    uarr.add(a[i]);
                }
                i++;
                
            }
			// If element of b is less and equal to element of a
            else {
                if(uarr.size()==0 || uarr.get(uarr.size()-1)!=b[j]){
                    uarr.add(b[j]);
                }
                j++;
            }
        }
		// Add remaining element from both array (only of these loop will run)
        while(i<a.length){
            if(uarr.get(uarr.size()-1)!=a[i]){
                uarr.add(a[i]);
    
            }
            i++;
        }
         while(j<b.length){
            if(uarr.get(uarr.size()-1)!=b[j]){
                uarr.add(b[j]);
            }
            j++;
        }
        return uarr;
         
    }
}

// Time Complexity: O(), Space Complexity: O()
```

## Python Solution
```Python
class Solution:
    #Function to return a list containing the union of the two arrays.
    def findUnion(self,arr1,arr2,n,m):
        '''
        :param a: given sorted array a
        :param n: size of sorted array a
        :param b: given sorted array b
        :param m: size of sorted array b
        :return:  The union of both arrays as a list
        '''
        # code here 
        s=set()
        for i in range(n):
            s.add(arr1[i])
        
        for i in range(m):
            s.add(arr2[i])
        
        return sorted(list(s))
```

## Python Solution
```Python
def sortedArray(a: [int], b: [int]) -> [int]:
    u = list(set(a).union(set(b))) # O((n + m)
    return sorted(u) # log(n + m)

// Time Complexity: O((n + m) log(n + m)) , Space Complexity: O(n + m)
```

# 10. [Missing Number]

## Java Solution - [Coding Ninja](https://www.codingninjas.com/studio/problems/missing-number_6680467?utm_source=striver&utm_medium=website&utm_campaign=codestudio_a_zcourse&leftPanelTab=1)
```Java
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
// Time Complexity: O(n), Space Complexity: O(1)
```

## Python Solution
```Python
class Solution:
    def missingNumber(self, nums: List[int]) -> int:
        for i in range(len(nums)+1):
            if (i not in nums):
                return i

// Time Complexity: O(), Space Complexity: O()
```
# 11. [Traffic]

## Java Solution
```Java

// Time Complexity: O(), Space Complexity: O()
```

## Python
```Python
```

# 12. [Find The Single Element]

## Java Solution - [Coding Ninja](https://www.codingninjas.com/studio/problems/find-the-single-element_6680465?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)

```Java
public class Solution {
    public static int getSingleElement(int []arr){
        int xor = 0;
        for (int i=0; i<arr.length; i++){
            xor = xor^arr[i];
        }
        return xor;
    }
}
// Time Complexity: O(n), Space Complexity: O(1)
```

## Python
```Python
class Solution:
    def singleNumber(self, nums: List[int]) -> int:
        xor=0
        for i in range(len(nums)):
            xor=xor^nums[i]
        return xor

# Time Complexity: O(n), Space Complexity: O(1)
```

# 13. [Longest Subarray With Sum K]

## Java Solution - [Coding Ninja](https://www.codingninjas.com/studio/problems/longest-subarray-with-sum-k_6682399?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)
```Java
public class Solution {
    public static int longestSubarrayWithSumK(int []a, long k) {
        int n = a.length;
        int mcount = 0; // maximum count
        for(int i=0; i<n; i++){
            long sum =0;  // sum (reset to 0 when j loop ends)
            int count = 0; // temp count
            for(int j=i; j<n; j++){
                sum+=a[j]; // sum until 
                count++;
                if (sum==k){
                    mcount = Math.max(count, mcount); // take maximum count
                }
                if (sum>k){ // if sum exceeds k then break loop
                    break;
                }
            }
        }
        return mcount;
    }
}

// Time Complexity: O(), Space Complexity: O()
```

## Python
```Python
```

# 14. [Longest Subarray With Sum K]

## Java Solution:
```Java

// Time Complexity: O(), Space Complexity: O()
```

## Python
```Python
```
```
```Java
```
