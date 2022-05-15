---
title: "Code Snippets"
tags:
- Software
- Explainer
enableToc: false
---

On this page I plan on documenting all the code snippets I use frequently. I'll use `T` for generic types, `K` for generic keys, and `V` for generic values when necessary. All of this code is written in `Java` since I think it's the most user-friendly.

# `HashMap` Iteration
```java
public void iterateHashMap(HashMap<K, V> map) {
    for (Map.Entry<K, V> entry : map.entrySet()) {
        entry.getKey();
        entry.getValue();
    }
}
```

# Depth-First Search
```java
public void dfs(HashSet<Node> visited, Node root) {
    if (root == null) {
        return;
    }

    visited.add(root);
    for (Node child : root.children) {
        if (!visited.contains(child)) {
            dfs(visited, child);
        }
    }
}

```
*This can be done iteratively with a stack instead of recursively.*

# Breadth-First Search
```java
public void bfs(Node root) {
    HashSet<Node> visited = new HashSet<>();
    Queue<Node> queue = new LinkedList<Node>();
    queue.add(root);

    while (!queue.isEmpty()) {
        Node curr = queue.poll();
        for (Node child : curr.children) {
            if (!visited.contains(child)) {
                queue.add(child);
                visited.add(child);
            }
        }
    }
}
```

# Level-Order Traversal
```java
public void levelOrder(Node root) {
    HashSet<Node> visited = new HashSet<>();
    Queue<Node> queue = new LinkedList<Node>();
    queue.add(root);

    int level = 0;
    while (!queue.isEmpty()) {
        int size = queue.size();
        for (int i = 0; i < size; i++) {
            Node curr = queue.poll();
            for (Node child : curr.children) {
                if (!visited.contains(child)) {
                    queue.add(child);
                    visited.add(child);
                }
            }
        }
        level++;
    }
}
```
*Level-order traversals differ from BFS because they keep track of what "step" of the BFS we're currently on. This can be handy for problems where we want to know the length of the shortest path, like [Word Ladder](https://leetcode.com/problems/word-ladder/) or [Rotting Oranges](https://leetcode.com/problems/rotting-oranges/)*.
