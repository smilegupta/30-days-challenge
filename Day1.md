### Date: July 01 2020

#### Total Questions solved: 3
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

#### Que2: https://leetcode.com/problems/sqrtx/
#### Tag: Binary Search Application
####  Solution:
````
class Solution {
public:
    int mySqrt(int x) {
       long long int l=0, r=x;
        long long int mid, ans;
        
        while(l<=r){
            mid=(l+r)/2;
            if((mid*mid)==x)
            {ans=mid; break;}
            if((mid*mid)<x)
            {   l=mid+1; ans=mid;}
            else 
                r=mid-1;
        }
        return ans;
    }
};
````

#### Que2: https://leetcode.com/problems/search-in-rotated-sorted-array/
#### Tag: Binary Search Application
####  Solution:
````
class Solution {
public:
    int search(vector<int>& nums, int target) {
        int n=nums.size();
        if(n==0)
            return -1;
        int i=0;
        int j=n-1;
        int m;
        while(i<=j)
        {
            m=(i+j)/2;
            if(nums[m]==target)
                return m;
            else if(nums[0]<=nums[m])
            {
                if(target>=nums[0]&&target<=nums[m])
                    j=m-1;
                else
                    i=m+1;
            }
            else
            {
                if(target>=nums[m]&&target<=nums[n-1])
                    i=m+1;
                else
                    j=m-1;
            }
        }
        return -1;
    }
};
````

