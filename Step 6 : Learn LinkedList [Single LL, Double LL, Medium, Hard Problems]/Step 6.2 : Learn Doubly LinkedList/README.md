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

# 2. [Insert at end of Doubly Linked List](https://www.codingninjas.com/studio/problems/insert-at-end-of-doubly-linked-list_8160464?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTabValue=PROBLEM)

### Solution
```Java
public class Solution
{
    public static Node insertAtTail(Node list, int K) {
        Node node = new Node(K); // Create a new node
        node.next = null; // Set node next address null as we are inserting at end
        if (list == null){ // If there is no node
            node.prev = null;   
            list = node; // Update head
            return list;
        }
        // Loop till last element
        Node temp = list; 
        while(temp.next!=null){
            temp = temp.next;
        }
        // Set address of node's prev and next
        node.prev = temp;
        temp.next = node;
        return list;   
    }
}
```

# 3. []()

### Solution
```Java
public class Solution{
    public static Node deleteLastNode(Node head) {
        // If there is only one node
        if (head.next==null){
            head = null;
            return head;
        }
        Node temp = head;
        // Traversing to the last node
        while(temp.next!=null && temp.next.next!=null){
            temp = temp.next;
        }
        // remove last node
        temp.next.prev = null; 
        temp.next = null;
        temp.prev = null;
        return head;
    }
}
// Time complexity: O(n), Space complexity: O(1)
```

# 4. []()

### Solution
```Java
```
