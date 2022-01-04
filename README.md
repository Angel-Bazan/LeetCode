# LeetCode 


### Description:
Given a non-empty array of integers nums, every element appears twice except for one. Find that single one.

You must implement a solution with a linear runtime complexity and use only constant extra space.




### Syntax:

```jsx
var singleNumber = function(nums) {
   return  nums.reduce((a, c) => c ^= a)
};
``` 

### Description: 
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

### Syntax: 

```jsx 
var twoSum = function(nums, target) {
    let map = new Map(); 
    for(let i = 0; i < nums.length ; i++){
        let num1 = nums[i]; 
        let num2 = target - num1 ; 
        
        if(map.has(num2)){
            return [i,map.get(num2)]
        }
        map.set(num1, i)
        
    }
    
};
```
