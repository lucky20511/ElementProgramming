### Compute Multiply without Arithmetic Operator

**Description/**

Compute A x B without using any arithmetic operators like + - \* /.

A and B are non-negative

**Variant/**

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

```
public long multiply(long x, long y) {























}
```

-------------------------------- Luckman -------------------------

**Thoughts/**

The key point is figure out how to do the add without arithmetic operator +. Use XOR and AND

**Code/**

```
public long multiply(long x, long y) {
    long ret = 0;
    for(int i = 0; i < 64; i++) {
        if(((y >> i) & 1) != 0) {
           ret = add(ret, x << i); 
        }
    }
    return ret;
}

private long add(long x, long y) {
    while(y != 0) {
        long left = x ^ y;
        long carry = (x & y) << 1;
        x = left;
        y = carry;
    }         
    return x;
}
```

-------------------------------- Author ------------------------------

**Thoughts/**

Use XOR and AND to replace the function of +

