# 1. [Introduction To Linked List](https://www.codingninjas.com/studio/problems/introduction-to-linked-list_8144737?utm_source=youtube&utm_medium=affiliate&utm_campaign=Codestudio_Linkedlistseries&leftPanelTabValue=PROBLEM)
## Java Solution
```Java
public class Solution {
    static Node head;
    public void insert(int value){
            Node node = new Node(value);
            node.next = head;
            head = node;
    }
    public static Node constructLL(int []arr) {
        Solution s = new Solution();
        for(int i=arr.length-1; i>=0; i--){
            s.insert(arr[i]);
        }
        
        return head;
    }
}
```

# 2. []()
## Java Solution
```Java
```

# 3 []()
## Java Solution
```Java
```

# 4. []()
## Java Solution
```Java
```

# 5. []()
## Java Solution
```Java
```
