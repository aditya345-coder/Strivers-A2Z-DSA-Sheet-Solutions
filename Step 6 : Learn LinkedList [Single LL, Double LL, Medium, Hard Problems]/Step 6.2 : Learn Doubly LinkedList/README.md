# 1. [Introduction To Doubly Linked List](https://www.codingninjas.com/studio/problems/introduction-to-doubly-linked-list_8160413?utm_source=youtube&utm_medium=affiliate&utm_campaign=Codestudio_Linkedlistseries&leftPanelTabValue=PROBLEM)

### Solution
```Java
public class Solution{
    public static Node constructDLL(int []arr) {
        Node head = null;
        for(int i=arr.length-1; i>=0; i--){
            Node node = new Node(arr[i]); // Create a node
            node.next = head; // asign node.next to head and node.prev is null
            if (head!=null){ // update the current head prev to new node
                head.prev = node;
            }
            head = node; // update head to point new node
         }
         return head;     
     }
}
```

# 2. []()

### Solution
```Java
```

# 3. []()

### Solution
```Java
```

# 4. []()

### Solution
```Java
```
