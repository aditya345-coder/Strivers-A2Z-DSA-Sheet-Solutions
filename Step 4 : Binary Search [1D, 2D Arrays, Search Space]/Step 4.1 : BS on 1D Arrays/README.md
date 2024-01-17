# 1. [Binary Search](https://www.codingninjas.com/studio/problems/binary-search_972?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution:
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
# 2. [Implement Lower Bound](https://www.codingninjas.com/studio/problems/lower-bound_8165382?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution:
```
```

# 3. [Implement Upper Bound](https://www.codingninjas.com/studio/problems/implement-upper-bound_8165383?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution:
```
```

# 4. [Search Insert Position](https://www.codingninjas.com/studio/problems/algorithm-to-find-best-insert-position-in-sorted-array_839813?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Solution:
```
```

# 5. [Floor/Ceil in Sorted Array]()
### Solution:
```
```

# 6. [Find the first or last occurrence in Array]()

### Solution:
```
```

# 7. [Count occurrences of a number in sorted array with duplicates]()

### Solution:
```
```

# 8. [Search in Rotated Sorted Array I]()

### Solution:
```
```

# 9. [Search in Rotated Sorted Array II]()

### Solution:
```
```

# 10. [Find minimum in Rotated Sorted Array]()

### Solution:
```
```

# 11. [Find out how many times has an array]()

### Solution:
```
```
	
# 12. [Single element in a Sorted Array]()

### Solution:
```
```

# 13. [Find peak element]()

### Solution:
```
```
