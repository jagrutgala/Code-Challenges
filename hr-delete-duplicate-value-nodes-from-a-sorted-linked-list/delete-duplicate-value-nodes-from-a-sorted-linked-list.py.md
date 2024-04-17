# Hacker Rank : delete-duplicate-value-nodes-from-a-sorted-linked-list

## 1

```py
#
# Complete the 'removeDuplicates' function below.
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

def removeDuplicates(head_node):
    # Write your code here
    values= set()
    node= head_node
    prev_node= None
    while node:
        print(f"set {values}")
        if(node.data not in values):
            values.add(node.data)
            prev_node= node
        else:
            # print(f"prev {prev_node.data} node {node.data}")
            prev_node.next= node.next
        node= node.next

    return head_node
```

Score: **5.00**
