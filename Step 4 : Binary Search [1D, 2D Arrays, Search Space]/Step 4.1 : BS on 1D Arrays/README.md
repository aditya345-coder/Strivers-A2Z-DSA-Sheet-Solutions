# 1. [Binary Search](https://leetcode.com/problems/binary-search/submissions/1423968544/)

## Java Solution: - [Coding Ninja](https://www.codingninjas.com/studio/problems/binary-search_972?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)
```
public class Solution {
    public static int search(int []nums, int target) {
        int n = nums.length;
        int low = 0; // low index
        int high = n-1; // high index
        
        // Loop untill low is less and equal to high
        while(low<=high){
            // Find middle index
            int mid = low + (high-low)/2;
            if (nums[mid]==target){
                return mid;
            }
            else if (target>nums[mid]){
                low = mid+1;
            }
            else{
                high = mid-1;
            }
        }
        return -1;
    }
}
```
## Python Solution:
```
class Solution:
    def search(self, nums: List[int], target: int) -> int:
        low=0; high=len(nums)-1
        while(low<=high):
            mid=low+(high-low)//2
            if (nums[mid]==target):
                return mid
            elif (nums[mid]>target):
                high=mid-1
            else:
                low=mid+1
        return -1
```

# 2. [Implement Lower Bound](https://www.geeksforgeeks.org/problems/floor-in-a-sorted-array-1587115620/1?track=DSASP-Searching&amp%253BbatchId=154&utm_source=youtube&utm_medium=collab_striver_ytdescription&utm_campaign=floor-in-a-sorted-array)

## Java Solution: [Coding Ninja](https://www.codingninjas.com/studio/problems/lower-bound_8165382?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)
```
public class Solution {
    public static int lowerBound(int []arr, int n, int x) {
        // Linear Search
        // int count = 0, res=0;
        // for(int i=0; i<n; i++){
        //     if (arr[i]<x){
        //         count++;
        //     }
        //     else if (arr[i]>=x){
        //         res = i;
        //         break;
        //     }
        // }
        // if (count==n){
        //     res = n;
        // }
        // return res;

        // Binary Search
        int low = 0, high = n-1;
        int ind = n;
        while(low<=high){
            int mid  = low + (high-low)/2;
            if (arr[mid]>=x && mid<ind ){
                ind = mid;
                high = mid -1;
            }
            else{
                low = mid + 1;
            }
        }
        return ind;
    }
}
```
## Python Solution:
```
class Solution:
    #User function Template for python3
    
    #Complete this function
    def findFloor(self,A,N,X):
        low=0; high=len(A)-1; floor=-1
        while(low<=high):
            mid = low + (high-low)//2
            if ((A[mid]<=X) and A[mid]>=floor):
                low=mid+1
                floor=mid
            elif (A[mid]>X):
                high=mid-1
                
        return floor

Time Complexity: O(logn) Space Complexity: O(1)
```

# 3. [Implement Upper Bound](https://www.geeksforgeeks.org/problems/ceil-the-floor2802/1)

## Java Solution:
```
class Solve {
    Pair getFloorAndCeil(int[] arr, int n, int x) {
        int low=0, high=arr.length-1;
        int floor=-1, ceil=-1;
        Arrays.sort(arr);
        while(low<=high){
            int mid = low + (high-low)/2;
            if (arr[mid]>x){
                high=mid-1;
                ceil = arr[mid];
            }
            else if (arr[mid]<x){
                low=mid+1;
                floor = arr[mid];
            }
            else{
                floor=arr[mid];
                ceil=arr[mid];
                break;
            }
            
        }
        return new Pair(floor, ceil);
    }
}

```
## Python Solution:
```
```

# 4. [Search Insert Position](https://www.codingninjas.com/studio/problems/algorithm-to-find-best-insert-position-in-sorted-array_839813?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

## Java Solution:
```
public class Solution {
    public static int searchInsert(int [] arr, int m){
        int n = arr.length;
        int low = 0, high = n-1;
        int ind = 0;

        while(low <= high){
            int mid = low + (high-low)/2;
            if (arr[mid]==m){
                return mid;
            }
            else if (arr[mid]>m) {
                high = mid - 1;
            }
            else{
                low = mid + 1;
            }
        }
        return low;
    }
}
```
## Python Solution:
```
```

# 5. [Floor/Ceil in Sorted Array](https://www.codingninjas.com/studio/problems/ceiling-in-a-sorted-array_1825401?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

## Java Solution:
```
import java.util.* ;
import java.io.*; 

public class Solution {
    public static int[] getFloorAndCeil(int[] a, int n, int x) {
        int [] res = new int[2];
        int floor = -1, ceiling = -1;
        int low = 0, high = n-1;
        
        // Order-Agnostic Binary Search 
        boolean asc = a[0]<a[n-1];
        while(low<=high){ // Loop until low index is less than or equal to high
           int mid = low+(high-low)/2; // Find mid element
           if (a[mid] == x){
              floor = a[mid];
              ceiling = a[mid];
              break;
           }
           // If ascending order
           else if (asc){
              if (a[mid]>x){
                high=mid-1;
                floor = a[mid];
              }
              else{
                low = mid+1;
                ceiling = a[mid];
              }
           }
           else{ // If descending order
              if (a[mid]<x){ //look for smaller index on the left
                high=mid-1;
                ceiling = a[mid];
              }
              else{ // look on the right
                low = mid+1;
                floor = a[mid];
              }
           }
        }
        // For ascending order
        // while(low<=high){
        //    int mid = low+(high-low)/2;
        //    if (a[mid] == x){
        //       floor = a[mid];
        //       ceiling = a[mid];
        //       break;
        //    }else if (a[mid]>x){
        //         high=mid-1;
        //         floor = a[mid];
        //    }
        //    else if (a[mid]<x){
        //      low = mid+1;
        //      ceiling = a[mid];
        //    }
        // }
        res[0] = ceiling;
        res[1] = floor;
        return res;
    } 
}
```
## Python Solution:
```
```

# 6. [Find the first or last occurrence in Array](https://www.codingninjas.com/studio/problems/first-and-last-position-of-an-element-in-sorted-array_1082549?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTabValue=SUBMISSION)

## Java Solution:
```
import java.util.* ;
import java.io.*; 
public class Solution {

    public static int[] firstAndLastPosition(ArrayList<Integer> arr, int n, int k) {
        int low = 0, high = arr.size()-1;
        int start_ind = -1, last_ind = -1;
        // Finding first occurance index
        while(low<=high){
            int mid  = low + (high-low)/2; // Mid eleemnet
            if (arr.get(mid) == k){
                start_ind = mid;
                high=mid-1; // shift to left
            }
            else if (arr.get(mid)>k){
                high = mid -1;
            }
            else{
                low = mid + 1;
            }
        }

        // finding last occurance index
        low = 0; high = arr.size()-1;
        while(low<=high){
            int mid  = low + (high-low)/2; // Mid eleemnet
            if (arr.get(mid) == k){ // If element is found
                last_ind = mid;
                low = mid + 1; // Shift to right
            }
            else if (arr.get(mid)>k){
                high = mid -1;
            }
            else{
                low = mid + 1;
            }
        }
        int [] a = {start_ind, last_ind};
        return a;
    }

};
```
## Python Solution:
```
def firstAndLastPosition(arr, n, k):
    low = 0 
    high = n-1
    start = -1
    end = -1
    # Lower Bound
    while(low<=high):
        mid = int(low+(high - low)/2)
        if (arr[mid]==k):
            start = mid
            high = mid - 1
        elif (arr[mid]>k):
            high = mid - 1
        else:
            low = mid + 1
    # Upper Bound
    low = 0 
    high = n-1
    while(low<=high):
      mid = int(low+(high - low)/2)
      if (arr[mid]==k):
          end = mid
          low = mid + 1
      elif (arr[mid]>k):
          high = mid - 1
      else:
          low = mid + 1
    
    return (start, end)

```

# 7. [Count occurrences of a number in sorted array with duplicates]()

## Java Solution:
```
```
## Python Solution:
```
```

# 8. [Search in Rotated Sorted Array I]()

## Java Solution:
```
import java.util.ArrayList;
public class Solution {
    public static int search(ArrayList<Integer> arr, int n, int k) {
        // Linear search
        // int index = -1;
        // for(int i=0; i<n; i++){
        //     if (arr.get(i)==k){
        //         index = i;
        //     }
        // }
        // return index;

        // Binary Search
        
        int index = 0; // rotationPoint
        // Search to find lowest element (from where the rotation is starting)
        int low = 0, high = n-1;
        while(low<high){
            int mid = low + (high-low)/2;
            if (arr.get(mid)>arr.get(high)){
                low = mid + 1;
            }
            else{
                high = mid;
            }  
        }
        // Search the element before rotationPoint window
        index = low;
        low = 0; high = index;
        while(low<=high){
            int mid = low + (high-low)/2;
            if (arr.get(mid)==k){
                return mid;
            }
            else if (arr.get(mid)>k){
                high = mid - 1;
            }
            else{
                low = mid + 1;
            }
        }
        // Search the element after the rotationPoint window
        low = index; high = n-1;
        while(low<=high){
            int mid = low + (high-low)/2;
            if (arr.get(mid)==k){
                return mid;
            }
            else if (arr.get(mid)>k){
                high = mid - 1;
            }
            else{
                low = mid + 1;
            }
        }
        return -1;
    }
}
// Time Complexity : O(log(N)), Space Complexity : O(1)
```
## Python Solution:
```
def search(arr, n, k):
    n = len(arr)
    # Find smallest element (find the rotated Position)
    low = 0; high = n-1
    while(low<high):
        mid = int(low + (high-low)//2)
        if (arr[mid]>arr[high]):
            low = mid + 1;
        else:
            high = mid;

    # Search before rotatedPositon
    rotatedPosition = low
    low = 0; high = rotatedPosition 
    while(low<=high):
        mid = int(low + (high-low)//2)
        if (arr[mid] == k):
            return mid
        elif (arr[mid]>k):
            high = mid-1
        else:
            low = mid+1
    # Search after rotatedPositon
    low = rotatedPosition; high = n-1
    while(low<=high):
        mid = int(low + (high-low)//2)
        if (arr[mid] == k):
            return mid
        elif (arr[mid]>k):
            high = mid-1
        else:
            low = mid+1
    return -1
# Time Complexity : O(log(N)), Space Complexity : O(1)
```

# 9. [Search in Rotated Sorted Array II]()

## Java Solution:
```
```
## Python Solution:
```
```

# 10. [Find minimum in Rotated Sorted Array]()

## Java Solution:
```
```
## Python Solution:
```
```

# 11. [Find out how many times has an array]()

## Java Solution:
```
```
## Python Solution:
```
```

# 12. [Single element in a Sorted Array]()

## Java Solution:
```
```
## Python Solution:
```
```

# 13. [Find peak element]()

## Java Solution:
```
```
## Python Solution:
```
```
