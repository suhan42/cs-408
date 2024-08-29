一般来说，递归实现DFS 算法又分为如下三种：

1）. 前序遍历(Pre-Order Traversal，根 - 左 - 右) ：指先访问根，然后访问子树的遍历方式

```java
private static <V> void dfs(TreeNode<V> tree, int depth) {
    if (d != null) {
        //打印节点值以及深度
        System.out.println(tree.getValue().toString() + ",   " + depth);
        
        if (tree.getChildList() != null && !tree.getChildList().isEmpty()) {
            for (TreeNode<V> item : tree.getChildList()) {
                dfs(item, depth + 1);
            }
        }
    }
}
```


2）. 后序遍历(Post-Order Traversal， 左 - 右 - 根)：指先访问子树，然后访问根的遍历方式

```java
private static <V> void dfs(TreeNode<V> tree, int depth) {
    if (d != null) {
        if (tree.getChildList() != null && !tree.getChildList().isEmpty()) {
            for (TreeNode<V> item : tree.getChildList()) {
                dfs(item, depth + 1);
            }
        }
        //打印节点值以及深度
        System.out.println(tree.getValue().toString() + ",   " + depth);
    }
}
```


3）. 中序遍历(In-Order Traversal， 左 - 根 - 右)：指先访问左（右）子树，然后访问根，最后访问右（左）子树的遍历方式。

中序遍历一般是用二叉树实现：

```java
private static <V> void dfs(TreeNode<V> root, int depth) {
    
    if (root.getLeft() != null){
        dfs(root.getLeft(), depth + 1);
    }
    //打印节点值以及深度
    System.out.println(d.getValue().toString() + ",   " + depth);
    
    if (root.getRight() != null){
        dfs(root.getRight(), depth + 1);
    }
}
```

