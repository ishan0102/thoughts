# Code Snippets
I'll use `Integer` as the data type for all of these snippets but they can be substituted with any data type.

Iterating over a `HashMap`
```java
Map<Integer, Integer> map = new HashMap<>();
for (Map.Entry<Integer, Integer> entry : map.entrySet()) {
	entry.getKey();
    entry.getValue();
}
```

BFS
```java
Queue<Integer> queue = new LinkedList<>();
queue.add(1);
while (!queue.isEmpty()) {
    
}
```

Level-Order BFS
```java
Queue<Integer> queue = new LinkedList<>();
queue.add(1);