Get the parity number of a binary word. If number of 1 bit is even, parity number is 0, otherwise is 1.

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

-------------------------------- Luckman -------------------------

**Thoughts/**

Count the number of 1 bit.

**Code/**

```
public short parity(long num) {
    short count = 0;
    while(num != 0) {
        num &= num-1;
        count ^= 1;
    }
    return count;
}
```

-------------------------------- Author ------------------------------

**Thoughts/**

Keep folding the number

01234567

         0123

             01

               0

