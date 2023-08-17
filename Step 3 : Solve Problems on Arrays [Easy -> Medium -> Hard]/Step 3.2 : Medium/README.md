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
