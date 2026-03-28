## Solution
```
class Solution {
public:
    void rotate(vector<int>& nums, int k) {
        int n = nums.size();
        vector<int> result(n);
        for (int i = 0; i < n; i++){
            int new_index = (i + k) % n;
            result[new_index] = nums[i];
        }
        nums = result;
    }
};
```
## Screenshot
<img width="1919" height="940" alt="Screenshot 2026-03-28 212727" src="https://github.com/user-attachments/assets/9462c921-8622-4206-88a4-7dea9a5069dd" />
