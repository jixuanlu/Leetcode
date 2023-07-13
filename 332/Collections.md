~~~
List<List<String>> ls;
// ls 为二维 list 其中内层 list 每个 list 只包含两个元素
// e.g. [["MUC","LHR"],["JFK","MUC"],["SFO","SJC"],["LHR","SFO"]]

Collections.sort(ls, (a, b) -> a.get(1).compareTo(b.get(1)));

// 可以通过 lambada 表达式将二维数组根据内层 list 的第二位排序
~~~
