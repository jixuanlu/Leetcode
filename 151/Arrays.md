~~~
Arrays.sort();     // input argument is an array
Arrays.asList();   // 可以直接将每个元素作为argument e.g. Arrays.asList(1, 2, 3);
Arrays.copyOfRange(array, startIndex, endIndex)  // 区间是[startIndex, endIndex)
Arrays.fill(array, object);  //将 Array 填满某个元素

nums = IntStream.of(nums)
		     .boxed()
		     .sorted((o1, o2) -> Math.abs(o2) - Math.abs(o1))
		     .mapToInt(Integer::intValue).toArray();
// 将数组按照绝对值从大到小进行排序
~~~
