# Hacker Rank : detect-whether-a-linked-list-contains-a-cycle

## 1

```py
# Complete the has_cycle function below.

#
# For your reference:
#
# SinglyLinkedListNode:
#     int data
#     SinglyLinkedListNode next
#
#
def has_cycle(head_node):
    node= head_node
    node_set= set()
    while node:
        if(node in node_set): return 1
        node_set.add(node)
        node= node.next
    return 0
```

Score: **5.00**

