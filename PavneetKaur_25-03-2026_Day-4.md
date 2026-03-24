## Soltion 1
```
class Solution {
public:
    int missingNumber(vector<int>& nums) {
        int length = nums.size();
        int result = 0;
        for (int i = 0; i <= length; i++){
            if (count(nums.begin(), nums.end(), i) < 1){
                result = i;
            }
        }
        return result;
    }
};
```
## Screenshot
<img width="1919" height="933" alt="image" src="https://github.com/user-attachments/assets/a8ba74c0-167b-4daf-84ee-52c5b72d75d2" />

## Solution 2
```
class Solution {
public:
    int missingNumber(vector<int>& nums) {
        int n = nums.size();
        int sum = n*(n+1)/2;
        int actual_sum = 0;
        for (int i = 0; i < n; i++){
            actual_sum = actual_sum + nums[i];
        }
        return sum - actual_sum;
    }
};
```
## Screenshot
<img width="1918" height="946" alt="image" src="https://github.com/user-attachments/assets/3a72a600-68f7-4ae6-83fd-5f9ce2a02484" />
