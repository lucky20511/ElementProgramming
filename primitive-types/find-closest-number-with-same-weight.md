### Find the Closest Number with Same Weight

**Description/**

Find the closest number with the same number of 1 bit

**Variant/**

Solve it in O\(1\)

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

```
public long closestNumber(long num) {
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
}

/****  Variant ****/

public long closestNumber(long num) {
   
}
```

-------------------------------- Luckman -------------------------

**Thoughts/**

Find the first bit which is different from next bit searching from the LSB

**Code/**

```
public long closestNumber(long num) {
    // num is non-negative and bigger than zero 
    for(int i = 0; i < ; i++) {
        if((num >> i) & 1 != (num >> (i + 1)) & 1) {
            return num ^ ((1L << i) | (1L << (i + 1)));
        }
    }
    // invalid input
    return 0;
}

/****  Variant ****/

public long closestNumber(long num) {
    // get find the first different bit 
    long overlap = (~num >> 1) & num;
    // get LSB 1 bit of overlap
    long smallestBit = overlap & -overlap;
    return num ^ (overlap | (overlap << 1));    
}
```

-------------------------------- Author ------------------------------

**Thoughts/**

