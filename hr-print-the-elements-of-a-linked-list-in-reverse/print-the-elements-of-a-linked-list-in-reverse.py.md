# Hacker Rank : print-the-elements-of-a-linked-list-in-reverse

## 1

```py
#
# Complete the 'reversePrint' function below.
#
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

def reversePrint(head_node):
    # Write your code here
    node= head_node
    stack= []
    while node:
        stack.append(node.data)
        node= node.next
    while stack:
        print(stack.pop())

```

Score: **5.00**(Accepted)
