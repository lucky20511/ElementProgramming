### Increment Integer

**Description/**

Increment an Integer represented as a array or list

**Variant/**

1. The sum of two numbers represented as string, and return the result as string as well

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

```
public List<Integer> incrementInteger(List<Integer> A) {






}


/**** Variant ****/

public String sumOfString(String A, String B) {






}
```

-------------------------------- Luckman -------------------------

**Thoughts/**

1. Basic addition manipulation: a + b = left + carry
2. index 0 is MSD, index size\(\) - 1 is LSD. Start from size\(\) - 1

   Variant/

3. Using StringBuilder append and then reverse at the end

4. while idxA &gt;= 0 \|\| idxB &gt;= 0 keep doing
5. check the carry at the end

**Code/**

```
public List<Integer> incrementInteger(List<Integer> A) {
    int i = A.size() - 1;
    int carry = 1;

    while(i >= 0 && carry != 0) {
        int cur = carry + A.get(i);
        carry = cur / 10;
        cur %= 10;
        A.set(i--, cur);   
    }
    if(carry != 0) {
        A.add(0, 1);
    }
    return A;            
}



/**** Variant ****/

public String sumOfString(String A, String B) {
    int idxA = A.length() - 1, idxB = B.length() - 1;
    int carry = 0;
    StringBuilder sb = new StringBuilder();
    while(idxA >= 0 || idxB >= 0) {
        int numA = (idxA >= 0) ? A.charAt(idxA--) - '0' : 0; 
        int numB = (idxB >= 0) ? B.charAt(idxB--) - '0' : 0; 
        int cur = numA + numB + carry;
        carry = cur / 10;
        cur %= 10;
        sb.append((char)(cur+'0'));
    }
    if(carry != 0) {
        sb.append('1');
    }
    return sb.reverse().toString();
}
```

-------------------------------- Author ------------------------------

**Thoughts/**

1. index 0 is MSD, index size\(\) - 1 is LSD. Start from size\(\) - 1
2. check the store the carry to the next digit and check the last\(index = 0\) digit to see if need one more digit '1'



