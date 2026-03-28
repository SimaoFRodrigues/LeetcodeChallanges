# 1. Two Sum

Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

 

### My solution:
```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        int soma = 0;
        int[] resposta = new int[2];
        for (int i = 0; i <= nums.length -1; i++){
            for (int j = 0; j <= nums.length -1; j++){
                soma = nums[i] + nums[j];
                if (soma == target && i != j){
                    resposta[0] = i;
                    resposta[1] = j;
                }
            }
        }
        return resposta;
    }
}
```