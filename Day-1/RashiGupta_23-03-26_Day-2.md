 vector<int> twoSum(vector<int>& nums, int target) {
        int n=nums.size();
        vector<int> v;
        for(int i=0; i<n; i++){
            for(int j=i+1; j<n; j++){

                if(nums[i]+nums[j]==target){
                    return {i,j};
                }
            }
        }
        return {};
    }
    
<img width="1904" height="907" alt="Screenshot 2026-03-23 224326" src="https://github.com/user-attachments/assets/c87d0be4-ebca-492b-8df9-c5d88a91a4f2" />

//Time complexity: O(n2)
//Space complexity: O(1).
