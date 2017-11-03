### Revese Bits

**Description/**

Reverse all bits in a number

**Variant/**

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

-------------------------------- Luckman -------------------------

**Thoughts/**

Construct the reversed number bit by bit.

**Code/**

```
public long reverseBits(long num) {
    long ret = 0;
    for(int i = 0; i < 64; i++) {
        ret = ret << 1 + ((num >> i) & 1);
    }
    return ret;
}
```

-------------------------------- Author ------------------------------

**Thoughts/**

1. Dived the 64-bit into 4 16-bit
2. Using the pre-computing table to do the reverse. 

```
    e.g. reversed   { {11} , {10} , {01} , {00} }
         original      00     01     10     11
```



