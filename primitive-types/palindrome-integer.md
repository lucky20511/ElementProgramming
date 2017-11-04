### Palindrome Integer

**Description/**

Judge if the integer is palindrome

**Variant/**

What if return value is int?

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

```
public long reverseDigits(int num) {



















}
```

-------------------------------- Luckman -------------------------

**Thoughts/**

Move the digits from LSD digits by digits to another value, and compare if they are the same.

Need to care about the conditions when number of digit is odd and number of digits is even.

**Code/**

```
public boolean isPalindrome(int num) {
    // if num == -inf
    if(num < 0) {
        return false;
    }
    int ret = 0;
    while(ret < num) {
        ret = ret * 10 + num % 10;
        // odd number of digits
        if(ret == num) {
            return true;
        }
        num /= 10;
    }
    // even number of digits
    return ret == num;    
}
```

-------------------------------- Author ------------------------------

**Thoughts/**

