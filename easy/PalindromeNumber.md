# 9. Palindrome Number
Given an integer x, return true if x is a palindrome, and false otherwise.

### My solution:
```java
class Solution {
    public boolean isPalindrome(int x) {
        String temp = Integer.toString(x);
        int[] array = new int[temp.length()];
        int num = Integer.parseInt(temp);
        // if negative
        if (num < 0){
            num = num * (-1);
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
        System.out.println("Resultado array: " + res + " Resultado inicial: " +num );
        if (res == num){
            System.out.println("True");
            return true;
        }
        return false;
    }
}
```
