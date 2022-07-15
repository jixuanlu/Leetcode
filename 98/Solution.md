# Recursion
Use the binary tree inorder traversal, for each node calculate the value from it pre node, if pre.val >= root.val return false, else update the pre to current root.
## Code
~~~
class Solution {
    TreeNode pre;
    public boolean isValidBST(TreeNode root) {
        if(root == null) return true;

        boolean left = isValidBST(root.left);
        if(!left) {
            return false;
        }

        if(pre != null && root.val <= pre.val) {
            return false;
        }
        pre = root;

        boolean right = isValidBST(root.right);
        return right;
    }
}
~~~
