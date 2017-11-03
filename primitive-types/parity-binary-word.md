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

**Code/**

```
public short parity(long num) {
   
   
   
   
   
   
   
   
   
   
   
   
   
}


/****  Variant ****/

public int addRightmostBits(int num) {



}

public int mod(int num, int p) {



}

public boolean isPowerTwo(int num) {



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



