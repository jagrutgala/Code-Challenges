# Hacker Rank : merge-two-sorted-linked-lists

## 1

```py
# Complete the mergeLists function below.

#
# For your reference:
#
# SinglyLinkedListNode:
#     int data
#     SinglyLinkedListNode next
#
#
def mergeLists(headA, headB):
    new_head= SinglyLinkedListNode(0)
    tail_node= new_head
    while True:
        if(headA is None):
            tail_node.next= headB
            break
        elif(headB is None):
            tail_node.next= headA
            break
        else:
            if(headA.data<= headB.data):
                tail_node.next= headA
                headA= headA.next
            else:
                tail_node.next= headB
                headB= headB.next
        tail_node= tail_node.next
    return new_head.next

```

Score: **5.00**(Accepted)
