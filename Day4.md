### Date: July 04 2020

#### Total Questions solved: 1
##### Que1: https://leetcode.com/problems/kids-with-the-greatest-number-of-candies/
###### Tag: Array -- Easy
##### Solution:

```
class Solution {
public:
    vector<bool> kidsWithCandies(vector<int>& candies, int extraCandies) {
        int max=candies[0];
        for(int i=0; i<candies.size(); i++){
            if(candies[i]>max)
                max=candies[i];
        }  
        
    vector<bool> ans(candies.size(), false);
    for(int i=0; i<candies.size(); i++)
    {
        if((candies[i]+extraCandies)>=max)
            ans[i]=true;
    }
    return ans;
    }
};
```
