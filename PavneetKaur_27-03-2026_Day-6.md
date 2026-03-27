## Solution
```
class Solution {
public:
    bool checkIfExist(vector<int>& arr) {
        unordered_set<int> seen;
        for (int i = 0; i < arr.size(); i++){
            if ((seen.count(arr[i]*2) > 0) || ((arr[i] % 2 == 0) && (seen.count(arr[i]/2) > 0))){
                return true;
            }
            else{
                seen.insert(arr[i]);
            }
        }
        return false;
    }
};
```
## Screenshot
<img width="1919" height="946" alt="image" src="https://github.com/user-attachments/assets/d96021a5-0728-44a8-b518-a40e202ceb1a" />
