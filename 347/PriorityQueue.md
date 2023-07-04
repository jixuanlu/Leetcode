~~~
PriorityQueue<Integer> pq = new PriorityQueue<>();
// PriorityQueue 默认是小根堆, 即将所有元素 poll() 出后是从小到大排列的

// 若要创建大根堆需要重写 compare 方法 或者用 lambada 表达式
PriorityQueue<Integer> pq = new PriorityQueue<>((o1, o2) -> o2 - o1);
// (o1, o2) -> o2 - o1 代表从大到小; (o1, o2) -> o1 - o2  代表从小到大.

// PriorityQueue 类型是数组可以这样写 (o1, o2) -> o1[1] - o2[1]) 代表按照 index 为 1 的数值排序
PriorityQueue<int[]> pq = new PriorityQueue<>((o1, o2) -> o1[1] - o2[1]);
~~~
| 返回值 | 方法 | 功能 |
| ------ | ----- | ----- |
| boolean | add(Element e) | 将指定元素插入到该优先级队列中 | 
| void | clear() | 从这个优先队列中移除所有元素 |
| boolean | contains(Object o) | 返回 true 如果此队列包含指定的元素 |
| Element | peek() | 检索但不删除这个队列头, 返回null如果队列为空(如果队列从小到大排列返回最小,反之返回最大) |
| Element | poll() | 检索并删除这个队列头, 返回null如果队列为空 |
| boolean | remove(Object o) | 从该队列中移除指定元素的一个实例如果它是存在的 |
| int | size() | 返回元素的个数 |
| Object[] | toArray() | 返回一个包含此队列中所有元素的数组 |


