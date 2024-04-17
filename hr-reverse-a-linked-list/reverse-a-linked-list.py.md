# Hacker Rank : reverse-a-linked-list

## 1

```py
#
# Complete the 'reverse' function below.
#
# The function is expected to return an INTEGER_SINGLY_LINKED_LIST.
# The function accepts INTEGER_SINGLY_LINKED_LIST llist as parameter.
#

#
# For your reference:
#
# SinglyLinkedListNode:
#     int data
#     SinglyLinkedListNode next
#
#

def reverse(head_node):
    # Write your code here
    node= head_node
    prev_node= None
    node_stack= []
    while node:
        node_stack.append(node)
        node= node.next
    head_node= node_stack.pop()
    node= head_node
    while node_stack:
        node.next= node_stack.pop()
        node= node.next
    node.next= None
    return head_node

```

Score: **5.00**(Accepted)
