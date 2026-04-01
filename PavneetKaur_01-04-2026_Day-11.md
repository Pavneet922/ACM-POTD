## Solution
```
class Solution {
public:
    ListNode* mergeTwoLists(ListNode* list1, ListNode* list2) {
        ListNode dummy(0);
        ListNode* tail = &dummy;
        while (list1 != nullptr && list2 != nullptr) {
            if (list1->val <= list2->val) {
                tail->next = list1;
                list1 = list1->next;
            } else {
                tail->next = list2;
                list2 = list2->next;
            }
            tail = tail->next;
        }
        if (list1 != nullptr) tail->next = list1;
        else tail->next = list2;

        return dummy.next;
    }
};
```
## Screenshot
<img width="1919" height="942" alt="image" src="https://github.com/user-attachments/assets/76db147e-2453-4b9b-a7e3-4ca1d7720a60" />
