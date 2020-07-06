### Date: July 03 2020

#### Total Questions solved: 2
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

##### Que2: https://leetcode.com/problems/peak-index-in-a-mountain-array/
###### Tag: Binary Search  -- Easy
##### Solution:

```
class Solution {
public:
    int peakIndexInMountainArray(vector<int>& A) {
        int size=A.size();
        int l=0; 
        int r=size-1;
        int mid;
       	while(l<=r)
       	{
       		mid=(l+r)/2;
       		if(A[mid]<A[mid+1])
       		{
       			l=mid+1;
			}
			else
			r=mid-1;
		}
		return l;
    }
};
```
