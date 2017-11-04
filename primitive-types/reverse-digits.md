### Reverse Digits

**Description/**

Reverse all digits of a number

**Variant/**

What if return value is int?

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

```
public long reverseDigits(int num) {



















}



/****  Variant ****/


public int reverseDigits(int num) {



}
```

-------------------------------- Luckman -------------------------

**Thoughts/**

Reverse it digit by digit

**Code/**

```
public long reverseDigits(int num) {
    long left = (num < 0) ? -num : num;
    long ret = 0;
    while(left != 0) {
        ret = ret * 10 + (left % 10);
        left /= 10;
    }
    return (num < 0) ? -ret : ret;
}



/****  Variant ****/

public int reverseDigits(int num) {
    // overflow
    if((-num * -1) != num) {
        return num;
    }
    int left = (num < 0) ? -num : num;
    int ret = 0;
    while(left != 0) {
        int next = ret * 10 + (left % 10);
        // overflow
        if((next / 10) != ret) {
            return num;
        }
        ret = next;
        left /= 10;
    }
    return (num < 0) ? -ret : ret;
}
```

-------------------------------- Author ------------------------------

**Thoughts/**

Reverse it digit by digit

