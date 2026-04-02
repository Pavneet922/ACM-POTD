## Solution
```
class Solution {
public:
    ListNode* deleteDuplicates(ListNode* head) {
        if (head == nullptr) return nullptr;
        ListNode* current = head;
        while (current->next != nullptr) {
            if (current->val == current->next->val) {
                current->next = current->next->next;
            } else {
                current = current->next;
            }
        }

        return head;
    }
};
```
## Screenshot
<img width="1919" height="942" alt="image" src="https://github.com/user-attachments/assets/fd828677-adac-484b-a29f-3448a97ce7bc" />
