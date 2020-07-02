### Date: July 02 2020

#### Total Questions solved: 1
##### Que1: https://leetcode.com/problems/find-peak-element/
###### Tag: Binary Search
##### Solution:
```
class Solution {
public:
    int findPeakElement(vector<int>& nums) {
        int left = 0;
        int right= nums.size()-1;
        if(nums.size() == 1)
            return 0;
        else{
         while(left<=right)
        {
            int mid = (left+right)/2;
            
            if(mid>0 && mid<nums.size()-1){
                if(nums[mid]>nums[mid+1] && nums[mid]>nums[mid-1])
                    return mid;
                else if(nums[mid-1]>nums[mid])
                    right=mid-1;
                else
                    left=mid+1;
                
            }
            else if(mid == 0)
            {
                if(nums[mid]> nums[mid+1]){
                    return mid;
                }
                else return mid+1;
            }
            else if(mid == nums.size()-1)
            {
                if(nums[mid]> nums[mid-1]){
                   return mid;
                }
                else return mid-1;
            }
        }
        }
        return -1;
    }
};
```
##### Que2: https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/
###### Tag: Binary Search
##### Solution:
```
class Solution {
public:
    int findMin(vector<int>& nums) {
        int left =0;
        int right = nums.size()-1;
        int mid;
        while(left<right){
            mid= (left+right)/2;
            if(mid>0 && nums[mid] < nums[mid-1])
                return nums[mid];
            else if(nums[left]<=nums[mid] && nums[mid]>nums[right] )
                left=mid+1;
            else
                right=mid-1;
        }
        return nums[left];
    }
};
```    
