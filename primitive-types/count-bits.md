### Count Number of 1 bit

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

-------------------------------- Luckman -------------------------

**Thoughts/**

111100

111011

**Code/**

```
public short countBits(int num) {
    short count = 0;
    while(num != 0) {
        num &= num-1;
        count++;
    }
    return count;
}
```

-------------------------------- Author ------------------------------

**Thoughts/**

Logic Shift

