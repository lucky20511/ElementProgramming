### Dutch National Flag \(Three way partition\)

**Description/**

Do the three way partition by given index i --&gt; A\[i\]

&lt; A\[i\]    = A\[i  \]  &gt;A\[i\]

**Variant/**

1.

2.

3.

4.

\[NOTE\]

**QuickSelect** or **QuickSort** can be implemented by both **2 way partition** or **3 way partition**

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

```
public void threeWayPartition(List<Integer> A) {



















}
```

-------------------------------- Luckman -------------------------

**Thoughts/**

```
1.Using three pointers:
   i -> first unclassified from the head
   j -> pointer to check each number 
   k -> first unclassified from the tail


2.for each iteration
   condition A:  nums[j] < pivot  --> swap i, j  and  i++, j++
   condition B:  nums[j] > pivot  --> swap j, k  and  k--   
   condition C:  nums[j] == pivot --> j++
   condition D:  j > k  --> break
```

**Code/**

```
public void threeWayPartition(List<Integer> A, int index) {
    int pivot = A.get(index);
    int i = 0, k = A.size() - 1;
    int j = 0;
    while(j <= k) {
        int cur = A.get(j);
        if(cur < pivot) {
            Collections.swap(A, i++, j++);
        } else if(cur > pivot) {
            Collections.swap(A, j, k--);
        } else { // cur == pivot
            j++;
        }
    }
}
```

-------------------------------- Author ------------------------------

**Thoughts/**

Author proposed many methods. But the best one for me is using the three pointers.

```
1.Using three pointers:
   i -> first unclassified from the head
   j -> pointer to check each number 
   k -> first unclassified from the tail


2.for each iteration
   condition A:  nums[j] < pivot  --> swap i, j  and  i++, j++
   condition B:  nums[j] > pivot  --> swap j, k  and  k--   
   condition C:  nums[j] == pivot --> j++
   condition D:  j > k  --> break
```



