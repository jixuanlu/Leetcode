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

```


# HashMap
HashMap is used to store key-value pairs, it don't allow duplicate keys, bu using "public Object put(Object Key, Object value)" to add elements to the map.

HashMap will be faster than HashSet. Since it use the unique key to get value.

~~~
HashMap<> map = new HashMap<>();

map.clear()

map.put(key, value);
//For put(), if we put an element that have the same key with the element that the map already exist, 
// it will match the value, if same don't change if different, overwrite the original value with the new value.

map.containsKey(Object key);

map.containsValue(Object value);

map.get(Object key); // return value;

map.isEmpty();

map.size();

map.remove(Object key);

map.replace(K key, V newValue);
~~~
