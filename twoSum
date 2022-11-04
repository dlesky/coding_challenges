//my initial solution was brute force with O(n^2).
//it was reasonably fast because the test input arrays were very small 
 
const twoSum = function(nums, target) {
    for (let i = 0; i<nums.length; i++) {
        for (let j = i+1; j<nums.length; j++ ) {
            if (nums[i]+nums[j] === target) {return [i,j]}
        }
    }
};


//this was inspired by solutions that I read about. This is O(n). 
//it involves building an array of the values that it has seen, essentially caching previous values and 
//uses the fact that there is only 1D of freedom (a+b = constant). 


function twoSum(nums,target) {
  let cache = {};
  let length = nums.length
  for (let i = 0; i<length;i++) {
    if ((cache[nums[i]]+nums[i])===target) {
      return [nums.indexOf(nums[i]),nums.lastIndexOf(cache[nums[i]])]
    } else {cache[target-nums[i]] = nums[i]};
  }  
}

//I think sorting is O~nlogn, which I didn't implment 
