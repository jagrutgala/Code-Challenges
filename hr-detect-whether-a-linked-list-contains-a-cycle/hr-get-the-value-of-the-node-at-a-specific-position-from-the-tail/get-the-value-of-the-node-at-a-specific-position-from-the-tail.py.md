# Hacker Rank : get-the-value-of-the-node-at-a-specific-position-from-the-tail

## 1

```py
#
# Complete the 'getNode' function below.
#
# The function is expected to return an INTEGER.
# The function accepts following parameters:
#  1. INTEGER_SINGLY_LINKED_LIST llist
#  2. INTEGER positionFromTail
#

#
# For your reference:
#
# SinglyLinkedListNode:
#     int data
#     SinglyLinkedListNode next
#
#

def getNode(head_node, positionFromTail):
    # Write your code here
    node= head_node
    llist2list= []
    while node:
        llist2list.append(node.data)
        node= node.next
    return llist2list[-(positionFromTail+1)]

```

Score: **5.00**
