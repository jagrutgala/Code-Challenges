# Leet Code 1 : middle-of-the-linked-list

## ts

```ts
/**
 * Definition for singly-linked list.
 * class ListNode {
 *     val: number
 *     next: ListNode | null
 *     constructor(val?: number, next?: ListNode | null) {
 *         this.val = (val===undefined ? 0 : val)
 *         this.next = (next===undefined ? null : next)
 *     }
 * }
 */

function middleNode(head: ListNode | null): ListNode | null {
    let fastNode: ListNode = head;
    let slowNode: ListNode = head;
    while (fastNode != null && fastNode.next != null) {
        fastNode = fastNode.next?.next;
        slowNode = slowNode.next;
    }
    return slowNode;
};
```

Time: **47ms**(93.12%)

Memory: **51.01MB**(81.27%)


## cs

```cs
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     public int val;
 *     public ListNode next;
 *     public ListNode(int val=0, ListNode next=null) {
 *         this.val = val;
 *         this.next = next;
 *     }
 * }
 */
public class Solution {
    public ListNode MiddleNode(ListNode head) {
        ListNode fastNode = head;
        ListNode slowNode = head;
        while (fastNode != null && fastNode.next != null) {
            fastNode = fastNode.next?.next;
            slowNode = slowNode.next;
        }
        return slowNode;
    }
}
```

Time: **59ms**(57.89%)

Memory: **40.05MB**(67.76%)
