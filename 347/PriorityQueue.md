~~~
PriorityQueue<Integer> pq = new PriorityQueue<>();
// PriorityQueue 默认是小根堆, 即将所有元素 poll() 出后是从小到大排列的

// 若要创建大根堆需要重写 compare 方法 或者用 lambada 表达式
PriorityQueue<Integer> pq = new PriorityQueue<>((o1, o2) -> o2 - o1);
// (o1, o2) -> o2 - o1 代表从大到小; (o1, o2) -> o1 - o2  代表从小到大.
~~~
| 返回值 | 方法 | 功能 |
| | -----|
