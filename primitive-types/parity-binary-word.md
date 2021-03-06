### Parity Binary Word

**Description/**

Get the parity number of a binary word. If number of 1 bit is even, parity number is 0, otherwise is 1.

**Variant/**

Do the following things in O\(1\)

1. \(01010000\)2 to \(01011111\)2
2. Compute x mod a power of two. e.g. 77 mod 64 = 13
3. Test if x is power of 2

-------------------------------- Leonard --------------------------

**Thoughts/**

Not count bit by bit; Only consider bits whose values are 1

**Code/**

```
public short parity(long num) {
    short res = 0;
    while (num != 0) {
        num &= num - 1;
        res ^= 1;
    }
    return res;
}


/****  Variant ****/

public int addRightmostBits(int num) {
    return num | (num - 1);
}

// p is the power of two
// ex. the power of two for 64 is 6
public int mod(int num, int p) {
    // p is a power of two
    return num & (1 << p - 1);    
}

public boolean isPowerTwo(int num) {
    return (num & (num - 1)) == 0;
    // num cannot be a negative num because it's a power of 2
}
```

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



/****  Variant ****/

public int addRightmostBits(int num) {
    return num | (num - 1);
}

public int mod(int num, int p) {
    return num & ((1 << p) - 1);
}

public boolean isPowerTwo(int num) {
    return num > 0 && (num & (num - 1)) == 0;
}
```

-------------------------------- Author ------------------------------

**Thoughts/**

Keep folding the number

```
01234567
    0123
      01
       0
```



