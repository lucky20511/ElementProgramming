Get the parity number of a binary word. If number of 1 bit is even, parity number is 0, otherwise is 1.

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

-------------------------------- Luckman -------------------------

**Thoughts/**

Count the number bit.

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

Logic Shift

