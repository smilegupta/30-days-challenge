### 30 Days of Continous CP Challenge:  Start Date: July 01 2020

#### Day1:
#### Total Questions solved: 1
##### Que1: https://leetcode.com/problems/binary-search/ 
###### Tag: Binary Search Algorithm
##### Solution:
```
class Solution {
public:
    int search(vector<int>& nums, int target) {
    int l, r, mid;
        l=0;
        r=nums.size()-1;
        
        while(l<=r){
            mid=(l+r)/2;
            if(nums[mid]==target)
                {
                return mid; 
                }
            if (nums[mid]>target)
            {
                r=mid-1;
            }
            else if (nums[mid]<target){
                l=mid+1;
            }
        }
        return -1;
        
    }
};
```

