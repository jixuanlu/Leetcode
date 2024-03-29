# Deque
~~~
Deque<Integer> deque = new LinkedList<Integer>();
~~~
| Return value | method | description |
| ------------ | ------ | ----------- |
| boolean | add(E e) | Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque) if it is possible to do so immediately without violating capacity restrictions, returning true upon success and throwing an IllegalStateException if no space is currently available. |
| void | addFirst(E e) | Inserts the specified element at the front of this deque if it is possible to do so immediately without violating capacity restrictions. |
| void | addLast(E e) | Inserts the specified element at the end of this deque if it is possible to do so immediately without violating capacity restrictions. |
| boolean | contains(Object o) | Returns true if this deque contains the specified element. |
| E | getFirst() | Retrieves, but does not remove, the first element of this deque. |
| E | getLast() | Retrieves, but does not remove, the last element of this deque. |
| boolean | offer(E e) | Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque) if it is possible to do so immediately without violating capacity restrictions, returning true upon success and false if no space is currently available. |
| boolean | offerFirst(E e) | Inserts the specified element at the front of this deque unless it would violate capacity restrictions. |
| boolean | 	offerLast(E e) | Inserts the specified element at the end of this deque unless it would violate capacity restrictions. |
| E | 	peek() | Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque), or returns null if this deque is empty. |
| E | peekFirst() | Retrieves, but does not remove, the first element of this deque, or returns null if this deque is empty. |
| E | peekLast() | Retrieves, but does not remove, the last element of this deque, or returns null if this deque is empty. |
| E	| poll() | Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), or returns null if this deque is empty. |
| E |	pollFirst() | Retrieves and removes the first element of this deque, or returns null if this deque is empty. |
| E	| pollLast() | Retrieves and removes the last element of this deque, or returns null if this deque is empty. |
| E |	pop() | Pops an element from the stack represented by this deque. |
| void | push(E e) | Pushes an element onto the stack represented by this deque (in other words, at the head of this deque) if it is possible to do so immediately without violating capacity restrictions, returning true upon success and throwing an IllegalStateException if no space is currently available. |
| E |	remove() | Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque). |
| boolean |	remove(Object o) | Removes the first occurrence of the specified element from this deque. |
| E |	removeFirst() | Retrieves and removes the first element of this deque. |
| boolean |	removeFirstOccurrence(Object o) | Removes the first occurrence of the specified element from this deque. |
| E |	removeLast() | Retrieves and removes the last element of this deque. |
| boolean | removeLastOccurrence(Object o) | Removes the last occurrence of the specified element from this deque. |
| int	| size() | Returns the number of elements in this deque. |
