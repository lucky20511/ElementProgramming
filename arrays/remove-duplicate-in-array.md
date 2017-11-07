### Remove Duplicate in Sorted Array

**Description/**

Remove duplicate in sorted array and return the new length of array

**Variant/**

1.Remove all the elements with specified value, and return the new length of array

2.Remove all the duplicate appear more than K times \(given\), and return the new length of array

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

```
public int removeDuplicate(List<Integer> A) {

}



/**** Variant ****/

public int removeTargetElement(List<Integer> A, int key) {

}


public int removeDuplicate(List<Integer> A, int t) {

}


```

-------------------------------- Luckman -------------------------

**Thoughts/**

The original method is to use another array to keep all classified element.

But we can do that in place by:

1.**Use one pointer i to keep the first index of unclassified element = tail of the new array**.

2.Use another pointer j to walk through each element in array and see if it is the same with the last classified element \[i-1\]

Variant/

Same idea --&gt; **Use one pointer i to keep the first index of unclassified element = tail of the new array**.

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

public int removeTargetElement(List<Integer> A, int key) {
    // check if A is empty
    int i = 0;
    for(int j = 0; j < A.size(); j++) {
        if(A.get(j) != key) {
            A.set(i++, A.get(j));
        }
    }
    return i;
}


public int removeDuplicate(List<Integer> A, int t) {
    // check if A is empty
    int i = 0;
    for(int j = 0; j < A.size(); j++) {
        if(i < t || A.get(j) != A.get(i - t)) {
            A.set(i++, A.get(j));
        }
    }
    return i;
}


```

-------------------------------- Author ------------------------------

**Thoughts/**

