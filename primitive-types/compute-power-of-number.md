### Compute Power of Number

**Description/**

Compute the x^y, where x is double y is int

**Variant/**

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

```
public double power(double x, int y) {




















}
```

-------------------------------- Luckman -------------------------

**Thoughts/**

X^13 = \(x\*x\)^6 \* x

**Code/**

```
public double power(double x, int y) {
    if(y == 0) {
        return 1;
    }
    if(y == 1) {
        return x;
    }
    if(y < 0) {
        return 1 / power(x, -y);
    }
    return power(x * x, y / 2) * power(x, y % 2);
}
```

-------------------------------- Author ------------------------------

**Thoughts/**

Not clearly understand

