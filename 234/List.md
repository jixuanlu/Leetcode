# List
~~~
List<Integer> list = new ArrayList<>();
~~~
| Return value | method | description |
|--------------|--------|-------------|
| boolean | 	add(E e) | Appends the specified element to the end of this list. |
| List<E> | subList(int fromIndex, int toIndex) | Returns a view of the portion of this list between the specified fromIndex, inclusive, and toIndex, exclusive. |
| void | clear() | Removes all of the elements from this list. |
| int | size() | Returns the number of elements in this list. |
| Object[] | toArray() | Returns an array containing all of the elements in this list in proper sequence (from first to last element). |
| boolean |	contains(Object o) | Returns true if this list contains the specified element. |
| E | set(int index, E element) | Replaces the element at the specified position in this list with the specified element. |
~~~
int[] array = list.stream().mapToInt(Integer::intValue).toArray();

// Convert an Integer list to an int array.
~~~
