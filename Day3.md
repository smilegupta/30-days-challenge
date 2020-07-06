### Date: July 03 2020

#### Total Questions solved: 1
##### Que1: https://leetcode.com/problems/search-insert-position/
###### Tag: Binary Search  -- Easy
##### Solution:

```
class Solution {
public:
    int searchInsert(vector<int>& nums, int target) {
        int left = 0;
        int right = nums.size()-1;
        int mid;
        while(left<=right){
            mid = left + (right-left)/2;
            if(nums[mid] == target)
                return mid;
            else if( nums[mid] < target)
                left = mid+1;
            else
                right = mid-1;
        }
        return left;
    }
};
```
