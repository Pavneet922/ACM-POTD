## Solution
```class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        int length = nums.size();
        for (int i = 0; i < length; i++){
            for (int j = i + 1; j < length; j++){
                if ((nums[i] + nums[j]) == target){
                    return {i, j};
                }
            }
        }
        return {};
    }
};
```
## Screenshot
<img width="1919" height="946" alt="image" src="https://github.com/user-attachments/assets/34a72baf-9184-404e-9554-94379c904094" />
