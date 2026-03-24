## Solution
```
class Solution {
public:
    int maxProfit(vector<int>& prices) {
        int profit = 0;
        int min_price = prices[0];
        for (int i = 1; i < prices.size(); i++){
            if (prices[i] <= min_price){
                min_price = prices[i];
            }
            else if (prices[i] - min_price > profit){
                profit = prices[i] - min_price;
            }
        }
        return profit;
    }
};
```
## Screenshot
<img width="1919" height="955" alt="image" src="https://github.com/user-attachments/assets/25529872-2c71-460d-8963-f8a50ed8c094" />
