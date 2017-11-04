### Compute Division only by Addition, Subtraction and Shift Operators

**Description/**

Compute Division only by Addition, Subtraction and Shift Operators

**Variant/**

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

```
public long division(long x, long y) {

}
```

-------------------------------- Luckman -------------------------

**Thoughts/**

x = y \* \(1011\) = y \* \(2^3 + 2^1 + 2^0\)

**Code/**

```
public long division(long x, long y) {
    // x / y
    int shift = -1;
    while((y << (shift + 1) <= x)) {
        shift++;
    }
    long ret = 0;
    y <<= shift;
    for(int i = shift; i >= 0; i--) {
        if(x >= y) {
            ret += 1 << i;
            x -= y;
        }
        y >>= 1;
    }
    return ret;
}
```

-------------------------------- Author ------------------------------

**Thoughts/**

