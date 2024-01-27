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
// Time Complexity: O(N), Space Complexity: O(N)
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
// Time Complexity: O(1), Space Complexity: O(1)
```

# 3 [Delete Node Of Linked List](https://www.codingninjas.com/studio/problems/delete-node-of-linked-list_8160463?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTabValue=PROBLEM)
## Java Solution
```Java
public class Solution {
    public static Node deleteLast(Node list){
        // Creating a dummy node 'head', and assigning it to 'list'
        Node head = list;
        // Getting second last element
        while (head.next != null && head.next.next != null){
            head = head.next;
        }

        // Assigning the 'next' of second last node 'NULL'.
        head.next = null;
        return list;
    }
}
// Time Complexity: O(N), Space Complexity: O(1)
```

# 4. [Count nodes of linked list](https://www.codingninjas.com/studio/problems/count-nodes-of-linked-list_5884?utm_source=youtube&utm_medium=affiliate&utm_campaign=Codestudio_Linkedlistseries&leftPanelTabValue=PROBLEM)
## Java Solution
```Java
public class Solution {
    public static int length(Node head){
        Node temp = head; // Create a temporary pointer
        int size = 0;
        while(temp!=null){ // loop until temp is null
            temp = temp.next;
            size+=1; // Increment size
        }
        return size;
    }
}
```

# 5. [Search in a Linked List](https://www.codingninjas.com/studio/problems/search-in-a-linked-list_975381?utm_source=youtube&utm_medium=affiliate&utm_campaign=Codestudio_Linkedlistseries&leftPanelTabValue=PROBLEM)
## Java Solution
```Java
public class Solution{
    public static int searchInLinkedList(Node head, int k){
        Node temp = head; // Create temporary pointer
        while(temp!=null){ // loop until temp is null
            if (temp.data == k){ // if found
                return 1;
            }
            temp = temp.next;
        }
        return 0;
    }
// Time Complexity: O(N), Space Complexity: O(1)
```
