class Solution {
    public int pivotIndex(int[] nums) {
        int sum=0;
        for(int i: nums){
            sum+=i;
        }
        int suml=0;
        int sumr = sum - nums[0];
        if(suml ==sumr) return 0;
        for(int i = 1; i < nums.length; i++){
            suml+=nums[i-1];
            sumr-=nums[i];
            if(suml == sumr) return i;
        }
        return -1;
    }
}