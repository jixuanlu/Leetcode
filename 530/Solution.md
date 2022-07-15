# Recursion
Use the binary tree inorder traversal, for each node calculate the absolute value from it pre node, if less than the global min update min to the abs value, 
finally return min.
## Code
~~~
class Solution {
    TreeNode pre;
    int result = Integer.MAX_VALUE;
    public int getMinimumDifference(TreeNode root) {
        if(root == null) return 0;
        traversal(root);
        return result;
    }

    public void traversal(TreeNode root){
        if(root == null) return;

        traversal(root.left);

        if(pre != null) {
            result = Math.min(result, root.val - pre.val);
        }
        pre = root;

        traversal(root.right);
    }
}
~~~
