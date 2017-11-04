### Generate Uniform Random Number

**Description/**

Generate uniform random number by using a coin, which can generate the 0 or 1 with the same probability.

**Variant/**

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

```
public int uniformRandom(int a, int b) {





















}
```

-------------------------------- Luckman -------------------------

**Thoughts/**

```
[1, 3]
 1  2  3  x
00 01 10 11

1st      2nd            3rd
1/4 + 1/4 * 1/4 + 1/4 * 1/4 * 1/4 + .....  = (1/4) / (3/4)  = 1/3 
```

1. change \[a, b\] to \[0, b-a \]  ,  b-a --&gt; c
2. calculate how many times of flipping the coin
3. flip the coin many times and update the count
4. If count exceed the c at the end, do all over again.
5. return count + a





**Code/**

```
public int uniformRandom(int a, int b) {
    // check if b-a <= 0     
   int high = b - a;
   if(high < 0) {
       return Integer.MAX_VALUE; 
   }
   int times = -1;
   while((1 << (times + 1)) < high) {
       times++;
   }
   int res = 0;
   do {
       res = 0;
       for(int i = 0; i < times; i++) {
           res |= flipCoin() << i;
       }   
   } while(res > high);
   return res + a;
}


private int flipCoin() {
    return (Math.random() < 0.5) ? 0 : 1;
}

```

-------------------------------- Author ------------------------------

**Thoughts/**

```
[1, 3]
 1  2  3  x
00 01 10 11

1st      2nd            3rd
1/4 + 1/4 * 1/4 + 1/4 * 1/4 * 1/4 + .....  = (1/4) / (3/4)  = 1/3 
```



