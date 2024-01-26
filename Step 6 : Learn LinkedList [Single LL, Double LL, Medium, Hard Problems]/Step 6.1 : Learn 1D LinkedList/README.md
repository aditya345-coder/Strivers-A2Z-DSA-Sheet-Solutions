# 1. [Introduction To Linked List](https://www.codingninjas.com/studio/problems/introduction-to-linked-list_8144737?utm_source=youtube&utm_medium=affiliate&utm_campaign=Codestudio_Linkedlistseries&leftPanelTabValue=PROBLEM)
## Java Solution
```Java
public class Solution {
    static Node head; // 'head' variable stores the head of the linked list
    public void insert(int value){
            Node node = new Node(value);   // Attach node to the "next" of the previous node
            node.next = head;
            head = node;
    }
    public static Node constructLL(int []arr) {
        Solution s = new Solution();
        for(int i=arr.length-1; i>=0; i--){
            s.insert(arr[i]); // insert function
        }
        return head;
    }
}
```

# 2. [ Insert Node At The Beginning](https://www.codingninjas.com/studio/problems/insert-node-at-the-beginning_8144739?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTabValue=PROBLEM)
## Java Solution
```Java
public class Solution
{
    public static Node insertAtFirst(Node list, int newValue) {
        // Make a node using 'newValue'
        Node new_node = new Node(newValue);
        // Assign 'list' to the next of 'new_node'
        new_node.next = list;
        return new_node;
    }
}
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
