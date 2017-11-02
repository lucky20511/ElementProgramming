### Count Number of 1 bit

-------------------------------- Leonard









-------------------------------- Luckman

**Thoughts/**

111100

111011

```
Public int countBits(int num) {
    int count = 0;
    while(num != 0) {
        num &= num-1;
        count++;
    }
    return count;
}
```



