### Swap Bits

**Description/**

Swap the ith and jth bit of a number.

**Variant/**

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

-------------------------------- Luckman -------------------------

**Thoughts/**

Compare the ith and jth bit. If they are the same, don't need to swap. If they are not the same, XOR 1 for this two bits.

**Code/**

```
public long swapBits(long num, int i, int j) {
    if(((num >> i) & 1) != ((num >> j) & 1)) {
        num ^= (1 << j) | (1 << i);
    }
    return num;
}
```

-------------------------------- Author ------------------------------

**Thoughts/**

Compare the ith and jth bit. If they are the same, don't need to swap. If they are not the same, XOR 1 for this two bits.

