# HashSet
HashSet is used to store objects, it don't allow duplicate elements, by using "public boolean add(Object obj)" to add elements to the set, if success return true else return false

```
HashSet<> set = new HashSet<>();

set.add(E e);

set.contains(Object o);

set.clear();

set.isEmpty();

set.remove(Object o);

set.size();

By doing set.iterator().next(); we can get the first element inside the set.
```


# HashMap
HashMap is used to store key-value pairs, it don't allow duplicate keys, bu using "public Object put(Object Key, Object value)" to add elements to the map.

HashMap will be faster than HashSet. Since it use the unique key to get value.

~~~
HashMap<> map = new HashMap<>();
~~~
| Return value | method | description |
|--------------|--------|-------------|
| void | map.clear() | Removes all of the mappings from this map. |
| V value | map.put(K key, V value) | For put(), if we put an element that has the same key as the element that the map already exists, it will match the value, if same doesn't change if different, overwrite the original value with the new value. |
| boolean | map.containsKey(Object key) |  |
| boolean | map.containsValue(Object value) |  |
| V | map.get(Object key) | return value |
| boolean | map.isEmpty() |  |
| int | map.size() |  |
| boolean | map.remove(Object key) |  |
| boolean | map.replace(K key, V newValue) |  |
| V | map.getOrDefault(key, defaultValue) | return the value if exist, otherwise return the default value. |
| Set<K> | map.keySet() | Returns a Set view of the keys contained in this map. |
| Collection<V> | map.values() | Returns a Collection view of the values contained in this map. |

~~~
List<Value> list = new ArrayList<Value>(map.values());

// Here the return type of map.values() is a Collection, and it can pass to List.
// The list will be a list that contains each value that map.values() contains.
// Collection 类的返回值可以作为其所有子类的输入, 例如 List, Queue, Deque, Map, Set.

HashSet<List<String>> set = new HashSet<>(map.values());
Deque<List<String>> deque = new LinkedList<>(map.values());

// This also works, but we have to make sure the datatype of the element in map.values() same with HashSet or Deque.
// In this case, would be List<String>


---------------------------------------------------------------------------------------------------------------------


for (Map.Entry<Integer,Integer> entry : map.entrySet()) {
    System.out.println("Key = " + entry.getKey() + " Value = " + entry.getValue());
}
// We can use this way to loop through the map.
~~~
