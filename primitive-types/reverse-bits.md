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

Compare the ith and jth bit. If they are the same, don't need to swap. If they are not the same, XOR 1 for this two bits.

