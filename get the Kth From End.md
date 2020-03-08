
https://leetcode-cn.com/problems/lian-biao-zhong-dao-shu-di-kge-jie-dian-lcof/

```java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) { val = x; }
 * }
 */
class Solution {

    
    public ListNode getKthFromEnd(ListNode head, int k) {
        ListNode temp=head;
        int count = 0;
        while(temp!=null){
          temp=temp.next;
          count++;  
        }      
        if(k<1||k>count) return null;
        ListNode p2 = head;
        for(int i = k; i<count;i++){
            p2 = p2.next;
        }
        return p2;
    }    
}
```
