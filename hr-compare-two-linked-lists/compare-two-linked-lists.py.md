# Hacker Rank : compare-two-linked-lists

## 1

```py
# Complete the compare_lists function below.

#
# For your reference:
#
# SinglyLinkedListNode:
#     int data
#     SinglyLinkedListNode next
#
#
def compare_lists(head_node1, head_node2):
    identical= 1
    node1= head_node1
    node2= head_node2
    while node1 or node2:
        if(node1.data != node2.data) or\
            (not node1.next and node2.next) or\
            (node1.next and not node2.next):
            identical= 0
            break
        node1= node1.next
        node2= node2.next
    return identical

```

Score: **5.00**(Accepted)
