# 9. Palindrome Number
Given an integer x, return true if x is a palindrome, and false otherwise.

### My solution:
```java
class Solution {
    public boolean isPalindrome(int x) {
        String temp = Integer.toString(x);
        int[] array = new int[temp.length()];
        // if negative
        if (Integer.parseInt(temp) < 0){
            temp = temp.substring(1);
        }
        // add to array
        for (int i = 0; i < temp.length(); i++) {
            array[i] = Character.getNumericValue(temp.charAt(temp.length() - 1 - i));
            System.out.println(array[i]);
        }
        int res = 0;
        for (int n :array){
            res = res * 10 + n;
        }
        if (res == Integer.parseInt(temp)){
            return true;
        }
        return false;
    }
}
```
