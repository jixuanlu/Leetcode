# Method 1 HashSet
Use HashSet to store each node, by the attribute of HashSet, if we can add the current node successfully, then the set don't exist such node, otherwise exist, 
which means there is a circle, inside the while loop we make head = head.next for each loop, if after loop all the node still no existed node, then the LinkedList 
don't have a circle. 
## Code
~~~
public class Solution {
    public boolean hasCycle(ListNode head) {
        Set<ListNode> seen = new HashSet<ListNode>();
        while(head != null) {
            if(!seen.add(head))
                return true;
            head = head.next;
        }
        return false;
    }
}
~~~

# Method 2 Fast and Slow pointer

## Code
~~~

~~~
