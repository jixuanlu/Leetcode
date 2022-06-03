# Method 1 HashSet
Similar with Question 141 we add each element to the Set, if we can't add successful, which means we go around a circle and went back to the first node in the circle,
then we can just return this node, otherwise if the current node == null we return null.
## Code
~~~
public class Solution {
    public ListNode detectCycle(ListNode head) {
        Set<ListNode> visited = new HashSet<ListNode>();
        while(head != null) {
            if(!visited.add(head))
                return head;
            head = head.next;
        }
        return null;
    }
}
~~~

# Method 2 Fast and Slow pointer

## Code
~~~
~~~
