### Count Number of 1 bit

**Description/**

count the number of 1 bit

**Variant/**

-------------------------------- Leonard --------------------------

**Thoughts/**

Arithmetic shift right "&gt;&gt;&gt;=" : 11111110 =&gt; 11111111

Logical shift right "&gt;&gt;=": 11111110 =&gt; 01111111

The difference between arithmetic shift right and logical shift right is that arithmetic shift care about sign.

Memorize "clear the lowermost set bit" =&gt; x & \(x - 1\)

"clear every bit except the lowermost set bit" =&gt; x & ~\(x - 1\)

**Code/**

```
// the following algorithm check every bit in the number no matter what a bit is (0 or 1)
// Luckman's idea only check bits whose value are 1. 
public short countBits(int num) {
    short count = 0;
    while (num != 0) {
        count += num & 1;
        num >>>= 1;   
    }
    return count;
}
```

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

