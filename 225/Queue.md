# Queue
~~~
Queue<Integer> queue = new LinkedList<>();
~~~
| Return value | method | description |
| ------------ | ------ | ----------- |
| boolean | offer(E e) | Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions. |
| boolean | add(E e) | Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions, returning true upon success and throwing an IllegalStateException if no space is currently available. |
| E | peek() | Retrieves, but does not remove, the head of this queue, or returns null if this queue is empty. |
| E | element() | Retrieves, but does not remove, the head of this queue. |
| E | poll() | Retrieves and removes the head of this queue, or returns null if this queue is empty. |
| E | remove() | Retrieves and removes the head of this queue. |
| int | size() | Return the size of the queue |
