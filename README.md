# Binary-Search-using-Java-Leetcode

    class Solution {
        public int binarySearch(int[] arr, int start,int end,int target){
            if(start<=end){
                int mid = start + (end-start)/2;
                if(arr[mid] == target){
                    return mid;
                }
                else if(target > arr[mid]){
                    return binarySearch(arr,mid+1,end,target);
                }
                else{
                    return binarySearch(arr,start,mid-1,target);
                }
            }
            return -1;
        }
        public int search(int[] nums, int target) {
            Solution obj = new Solution();
            int n = nums.length-1; 
            int result = obj.binarySearch(nums,0,n,target);
            return result;
        }
    }
