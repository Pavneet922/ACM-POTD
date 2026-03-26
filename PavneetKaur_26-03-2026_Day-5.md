## Solution
```
class Solution {
public:
    void moveZeroes(vector<int>& nums) {
        int length = nums.size();
        int j = 0;
        for (int i = 0; i < length; i++){
            if (nums[i] != 0){
                nums[j] = nums[i];
                j++;
            }
        }
        for (int k = j; k < length; k++){
            nums[k] = 0;
        }
    }
};
```
## Screenshot
<img width="1919" height="948" alt="Screenshot 2026-03-26 200910" src="https://github.com/user-attachments/assets/e3dda9b8-6822-4cd1-ae1a-81ef0fe89c33" />
