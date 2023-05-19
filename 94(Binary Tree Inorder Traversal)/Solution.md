# Binary Tree Inorder Traversal (中序遍历)
左节点  根节点  右节点
# Method 1 Recursion

## Code
~~~
class Solution {
    public List<Integer> inorderTraversal(TreeNode root) {
        List<Integer> res = new ArrayList<>();
        traversal(root, res);
        return res;
    }

    public void traversal(TreeNode root, List<Integer> res) {
        if(root == null)
            return;
        traversal(root.left, res);
        res.add(root.val);
        traversal(root.right, res); 
    }
}
~~~

# Method 2 Iteration
从根节点一直遍历到最左边的子节点，并将每一个子节点放入栈，顺序pop出每一个子节点将其值存入list然后将root的右节点赋值给root重复以上操作，这样就可以在栈中存储每一个父节点的信息，每当遍历完右子树，pop出的结果就是当前子树的根的父节点，将其赋值给root后进行下一次迭代。
## Code
~~~
class Solution {
    public List<Integer> inorderTraversal(TreeNode root) {
        List<Integer> res = new ArrayList<Integer>();
        Deque<TreeNode> stack = new LinkedList<TreeNode>();
        while(root != null || !stack.isEmpty()){
            while(root != null) {
                stack.push(root);
                root = root.left;
            }
            root = stack.pop();
            res.add(root.val);
            root = root.right;
        }
        return res;
    }
}
~~~
