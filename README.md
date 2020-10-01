# Shortest-Unsorted-Continuous-Subarray
Given an integer array, you need to find one continuous subarray that if you only sort this subarray in ascending order, then the whole array will be sorted in ascending order, too.
class Solution {
    public int findUnsortedSubarray(int[] nums) {
       int l = nums.length; 
        int r =0;
        for(int i=0;i<nums.length-1;i++){
            for(int j=i+1;j<nums.length;j++){
                if(nums[i]>nums[j]){
                   r=Math.max(r,j);
                    l=Math.min(l,i);
            }
        }
    
    }
        return r-l<0 ? 0 : r-l+1;
}
}
