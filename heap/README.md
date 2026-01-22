# Heap Module

A min-heap (priority queue) implementation for EZ. Always returns the lowest priority item first.

## What is a Heap?

A heap is a binary tree stored as an array where the parent is always smaller (min-heap) or larger (max-heap) than its children.

```
Array:  [1, 2, 3, 5, 7, 4, 6]

Tree representation:

           [1]              <- index 0 (root, smallest)
          /   \
        [2]   [3]           <- indices 1, 2
        / \   / \
      [5][7] [4][6]         <- indices 3, 4, 5, 6
```

### Index Math

For any index `i`:
- Parent index: `(i - 1) / 2`
- Left child index: `(2 * i) + 1`
- Right child index: `(2 * i) + 2`

### Min-Heap Rule

Parent's priority is ALWAYS <= children's priorities. This means the smallest priority is always at index 0 (the root).

## How Operations Work

### Push (Insert)

1. Add new item to the end of the array
2. "Bubble up": Compare with parent, swap if smaller, repeat until in correct position

```
Insert priority 1 into [2, 5, 3]:

Step 1: Add to end      -> [2, 5, 3, 1]
Step 2: Compare 1 < 5   -> swap -> [2, 1, 3, 5]
Step 3: Compare 1 < 2   -> swap -> [1, 2, 3, 5]
Step 4: At root, done!
```

### Pop (Remove)

1. Save the root (smallest item)
2. Move last item to root
3. "Bubble down": Compare with children, swap with smallest child, repeat until in correct position

```
Pop from [1, 2, 3, 5]:

Step 1: Save root (1), move last to root -> [5, 2, 3]
Step 2: Compare 5 with children (2, 3)   -> 2 is smallest, 5 > 2, swap -> [2, 5, 3]
Step 3: Index 1 has no children, done!
Result: Returns 1, heap is now [2, 5, 3]
```

## Usage

### Creating a Heap

```ez
Simply copy the `heap` directory into your ptojects structure
Then, in the file you plan on using the `heap` modules functions or constants write the following at the top of said file:

import "relative/path/to/heap"

temp yourHeapVariable [heap.HeapItem]
```

### Pushing Items

```ez
// Push with priority and value (lower priority = comes out first)
heap.push_string(tasks, 1, "Urgent task")
heap.push_string(tasks, 5, "Low priority task")
heap.push_string(tasks, 3, "Medium task")
heap.push_int(tasks, 2, 42)
```

### Popping Items

```ez
temp item = heap.pop(tasks)  // Returns "Urgent task" (priority 1)

// Extract the value
if heap.item_is_string(item) {
    temp value = heap.get_string(item)
    temp priority = heap.get_priority(item)
    println("Got: ${value} with priority ${priority}")
}
```

### Other Operations

```ez
temp top = heap.peek(tasks)      // View top without removing
temp empty = heap.is_empty(tasks) // Check if empty
temp count = heap.size(tasks)     // Get item count
```

## API Reference

### Push Functions
| Function | Description |
|----------|-------------|
| `push_string(&heap, priority, value)` | Push a string value |
| `push_int(&heap, priority, value)` | Push an int value |
| `push_float(&heap, priority, value)` | Push a float value |
| `push_bool(&heap, priority, value)` | Push a bool value |

### Core Operations
| Function | Description |
|----------|-------------|
| `pop(&heap) -> HeapItem` | Remove and return highest priority item |
| `peek(heap) -> HeapItem` | View highest priority item without removing |
| `is_empty(heap) -> bool` | Check if heap is empty |
| `size(heap) -> int` | Get number of items |

### Value Extraction
| Function | Description |
|----------|-------------|
| `get_priority(item) -> int` | Get item's priority |
| `get_type(item) -> int` | Get type (0=string, 1=int, 2=float, 3=bool) |
| `item_is_string(item) -> bool` | Check if value is string |
| `item_is_int(item) -> bool` | Check if value is int |
| `item_is_float(item) -> bool` | Check if value is float |
| `item_is_bool(item) -> bool` | Check if value is bool |
| `get_string(item) -> string` | Extract string value |
| `get_int(item) -> int` | Extract int value |
| `get_float(item) -> float` | Extract float value |
| `get_bool(item) -> bool` | Extract bool value |

## Potential Use Cases

- **Task scheduling**: Always run highest priority task next
- **Event simulation**: Process events in time order
- **Finding top K items**: Top 10 scores, cheapest 5 options
- **Pathfinding**: Dijkstra's algorithm for shortest path
