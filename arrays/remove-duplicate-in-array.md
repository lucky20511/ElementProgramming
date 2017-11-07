### Remove Duplicate in Array

**Description/**

Remove duplicate in array and return the new length of array

**Variant/**



-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

```

```

-------------------------------- Luckman -------------------------

**Thoughts/**

The original method is to use another array to keep all classified element.

But we can do that in place by:

1.Use one pointer i to keep the first index of unclassified element.

2.Use another pointer j to walk through each element in array and see if it is the same with the last classified element \[i-1\]

Variant/



**Code/**

```
public int removeDuplicate(List<Integer> A) {
    // check if A is empty
    int i = 0;
    for(int j = 0; j < A.size(); j++) {
        if(i == 0 || A.get(j) != A.get(i - 1)) {
            A.set(i++, A.get(j));
        }
    }
    return i;
}



/**** Variant ****/


```

-------------------------------- Author ------------------------------

**Thoughts/**

