class Solution {
    public boolean isTrionic(int[] nums) {
        int n = nums.length;
        
        // Find p: first position where array stops increasing
        int p = 0;
        while (p < n - 1 && nums[p] < nums[p + 1]) {
            p++;
        }
        
        // p must be > 0 (there must be an increasing section)
        if (p == 0) {
            return false;
        }
        
        // Find q: first position after p where array stops decreasing
        int q = p;
        while (q < n - 1 && nums[q] > nums[q + 1]) {
            q++;
        }
        
        // q must be > p (there must be a decreasing section)
        if (q == p) {
            return false;
        }
        
        // q must be < n - 1 (there must be an increasing section after q)
        if (q == n - 1) {
            return false;
        }
        
        // Check that the rest is strictly increasing
        for (int i = q; i < n - 1; i++) {
            if (nums[i] >= nums[i + 1]) {
                return false;
            }
        }
        
        return true;
    }
}
