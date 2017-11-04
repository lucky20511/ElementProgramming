### Palindrome Integer

**Description/**

Judge if the integer is palindrome

e.g.

0 --&gt; true

-1 --&gt; false

7 --&gt; true

11 --&gt; true

17 --&gt; false

**Variant/**

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

```
public boolean isPalindrome(int num) {




















}
```

-------------------------------- Luckman -------------------------

**Thoughts/**

Move the digits from LSD digits by digits to another value, and compare if they are the same.

Need to care about the conditions when number of digit is odd and number of digits is even.

**Code/**

```
public boolean isPalindrome(int num) {
    // if num is negative
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

Calculate the number of digits by Math.log10\(\) and then compare just like String by using two pointer head and tail.

