## Solution
```

class Solution {
public:
    ListNode* middleNode(ListNode* head) {
        ListNode* slow = head, *fast = head;
        while (fast && fast->next) {
            slow = slow->next;
            fast = fast->next->next;
        }
        return slow;
    }
};
```
## Screenshot
<img width="1919" height="944" alt="image" src="https://github.com/user-attachments/assets/59c15529-86d6-444d-adf1-cf573f26a0a2" />
