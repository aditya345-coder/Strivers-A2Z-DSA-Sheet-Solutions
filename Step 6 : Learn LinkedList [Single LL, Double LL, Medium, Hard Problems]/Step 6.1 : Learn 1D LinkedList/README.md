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

# 2. [ Insert Node At The Beginning](https://www.geeksforgeeks.org/problems/linked-list-insertion-1587115620/0)
## Java Solution
```Java
class Solution
{
    //Function to insert a node at the beginning of the linked list.
    Node insertAtBeginning(Node head, int x)
    {
        Node newNode = new Node(x);
        if (head==null){
            head=newNode;
            return head;
        }
        newNode.next = head;
        head=newNode;
        return head;
    }
    
    //Function to insert a node at the end of the linked list.
    Node insertAtEnd(Node head, int x)
    {
        Node newNode = new Node(x);
        if (head==null){
            head=newNode;
            return head;
        }
        Node tail = head;
        while(tail.next!=null){
            tail = tail.next;
        }
        tail.next = newNode;
        return head;
    }
}
// Time Complexity: O(1), Space Complexity: O(1)
```

# 3 [Delete Node Of Linked List](https://leetcode.com/problems/delete-node-in-a-linked-list/description/)
## Java Solution
```Java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) { val = x; }
 * }
 */
class Solution {
    public void deleteNode(ListNode node) {
        ListNode temp = node;
        while(temp.next!=null)
        {
            temp.val = temp.next.val;
            if (temp.next.next==null){
                temp.next=null;
            }else{
                temp=temp.next;
            }
        }
    }
}
// Time Complexity: O(N), Space Complexity: O(1)
```

# 4. [Count nodes of linked list](https://www.geeksforgeeks.org/problems/count-nodes-of-linked-list/0)
## Java Solution
```Java
class Solution
{
    //Function to count nodes of a linked list.
    public static int getCount(Node head)
    {
        int size=0;
        while(head!=null){
            size++;
            head=head.next;
        }
        return size;
    }
}
```

# 5. [Search in a Linked List](https://www.geeksforgeeks.org/problems/search-in-linked-list-1664434326/1)
## Java Solution
```Java
/* Node of a linked list
  class Node {
   int data;
    Node next;
    Node(int d)  { data = d;  next = null; }
}
*/
class Solution {
    static boolean searchKey(int n, Node head, int key) {
        while(head.next!=null){
            if (head.data == key){
                return true;
            }
            head=head.next;
        }
        return false;
    }
}
// Time Complexity: O(N), Space Complexity: O(1)
```
