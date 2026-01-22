# Stack Module

A LIFO (Last In, First Out) stack data structure implementation for EZ.

## What is a Stack?

A stack is a linear data structure where elements are added and removed from the same end (the "top"). Think of it like a stack of plates - you can only add or remove plates from the top.

```
Push 1, Push 2, Push 3:

  +---+
  | 3 |  <- top (last in, first out)
  +---+
  | 2 |
  +---+
  | 1 |
  +---+

Pop returns 3, then 2, then 1
```

### LIFO Principle

- **Last In, First Out**: The most recently added item is the first to be removed
- Push adds to the top
- Pop removes from the top

## Usage

### Creating a Stack

```ez
Simply copy the `stack` directory into your projects structure
Then, in the file you plan on using the `stack` modules functions or constants write the following at the top of said file:

import "relative/path/to/stack"

temp myStack [stack.StackItem]
```

### Pushing Items

```ez
// Push different types onto the stack
stack.push_string(myStack, "first")
stack.push_string(myStack, "second")
stack.push_int(myStack, 42)
stack.push_float(myStack, 3.14)
stack.push_bool(myStack, true)
```

### Popping Items

```ez
temp item = stack.pop(myStack)  // Returns true (last pushed)

// Extract the value based on type
if stack.item_is_bool(item) {
    temp value = stack.get_bool(item)
    println("Got bool: ${value}")
}
```

### Peeking

```ez
// View top item without removing it
temp top = stack.peek(myStack)
```

### Other Operations

```ez
temp empty = stack.is_empty(myStack)  // Check if empty
temp count = stack.size(myStack)       // Get item count
stack.clear(myStack)                   // Remove all items
```

## API Reference

### Push Functions

| Function | Description |
|----------|-------------|
| `push_string(&stack, value string)` | Push a string onto the stack |
| `push_int(&stack, value int)` | Push an int onto the stack |
| `push_float(&stack, value float)` | Push a float onto the stack |
| `push_bool(&stack, value bool)` | Push a bool onto the stack |

### Core Operations

| Function | Description |
|----------|-------------|
| `pop(&stack) -> StackItem` | Remove and return top item |
| `peek(stack) -> StackItem` | View top item without removing |
| `is_empty(stack) -> bool` | Check if stack is empty |
| `size(stack) -> int` | Get number of items |
| `clear(&stack)` | Remove all items from stack |

### Type Checking

| Function | Description |
|----------|-------------|
| `get_type(item) -> (int, string)` | Get type (0=string, 1=int, 2=float, 3=bool) |
| `item_is_string(item) -> bool` | Check if value is string |
| `item_is_int(item) -> bool` | Check if value is int |
| `item_is_float(item) -> bool` | Check if value is float |
| `item_is_bool(item) -> bool` | Check if value is bool |

### Value Extraction

| Function | Description |
|----------|-------------|
| `get_string(item) -> string` | Extract string value |
| `get_int(item) -> int` | Extract int value |
| `get_float(item) -> float` | Extract float value |
| `get_bool(item) -> bool` | Extract bool value |

## Potential Use Cases

- **Undo/Redo functionality**: Push actions onto stack, pop to undo
- **Expression evaluation**: Evaluate postfix/prefix expressions
- **Balanced parentheses**: Check if brackets are properly matched
- **Backtracking algorithms**: Store states to backtrack to
- **Call stack simulation**: Track function calls
- **Browser history**: Back button functionality (within a session)
