### Multiply Big Integer

**Description/**

Multiply

**Variant/**

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

```
public List<Integer> Multiply(List<Integer> A, List<Integer> B) {











}
```

-------------------------------- Luckman -------------------------

**Thoughts/**

1. Take the sign of result, and make A\[0\] and B\[0\] to positive
2. Use array to store the value temporarily and handle the carry and leading zero at the end.
3. ith x jth  = i+j th

**Code/**

```
public List<Integer> Multiply(List<Integer> A, List<Integer> B) {
    // check if A and B are empty
    int lenA = A.size(), lenB = B.size();
    if(lenA == 0 || lenB == 0) {
         return new ArrayList<Integer>();
    }
    
    int sign = 1;
    if(A.get(0) * B.get(0) < 0) {
         sign = -1;
    }
    if(A.get(0) < 0) {
         A.set(0, -A.get(0));
    }
    if(B.get(0) < 0) {
         B.set(0, -B.get(0));
    }
    
    int len = lenA + lenB;
    int[] ret = new int[len];
    for(int i = 0; i < lenA; i++) {
         for(int j = 0; j < lenB; j++) {
              ret[len - 1 - i - j] += A.get(lenA - 1 - i) * B.get(lenB - 1 - j);
         }
    }
    for(int i = len - 1; i >= 1; i--) {
         ret[i - 1] += ret[i] / 10;
         ret[i] %= 10; 
    }
    int start = 0;
    while(ret[start] == 0) {
         start++;
    } 

    List<Integer> list = new ArrayList<>();
    for(int i = start; i < len; i++) {
         if(i == start) {
              list.add(sign * ret[i]);
         } else {
              list.add(ret[i]);
         }
    }                       
    return list;                        
}
```

-------------------------------- Author ------------------------------

**Thoughts/**

