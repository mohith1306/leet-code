/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode() {}
 *     TreeNode(int val) { this.val = val; }
 *     TreeNode(int val, TreeNode left, TreeNode right) {
 *         this.val = val;
 *         this.left = left;
 *         this.right = right;
 *     }
 * }
 */
import java.util.ArrayList;
import java.util.List;

class Solution {
    public void rec(TreeNode root, String path, List<String> result) {
        if (root == null) return;
        path += root.val;
        if (root.left == null && root.right == null) {
            result.add(path);
        } else {
            path += "->";
            rec(root.left, path, result);
            rec(root.right, path, result);
        }
    }
    public List<String> binaryTreePaths(TreeNode root) {
        List<String> result = new ArrayList<>();
        rec(root, "", result);
        return result;
    }
}
