## Solution
```
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode() : val(0), next(nullptr) {}
 *     ListNode(int x) : val(x), next(nullptr) {}
 *     ListNode(int x, ListNode *next) : val(x), next(next) {}
 * };
 */
class Solution {
public:
    ListNode* reverseList(ListNode* head) {
        if (head == nullptr or head -> next == nullptr) {
            return head;
        }
        ListNode *prev = nullptr;
        ListNode *current = head;
        
        while (current != nullptr){
            ListNode *next = current -> next;
            current -> next = prev;
            prev = current;
            current = next;

        }
        return prev;
    }
};
```
## Screenshot
<img width="1919" height="945" alt="image" src="https://github.com/user-attachments/assets/85aa96eb-c1e6-46bc-957d-e11316df4625" />
