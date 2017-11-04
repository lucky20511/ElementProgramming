### Even Odd Change

**Description/**

Given an array, you need rearrange array so that the entries with even number appear first

e.g.

1 2 3 5 0 3 5 2  --&gt; 2 0 2 1 3 5 3 5

**Variant/**

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

```
public void evenOddChange(List<Integer> A) {






}
```

-------------------------------- Luckman -------------------------

**Thoughts/**

```
1.Two pointer: head and tail.      
      head -> first unclassified number from head     
      tail -> first unclassified number from tail

2.For each iteration
      condition A : num[head] is even --> head++
      condition B : num[head] is odd --> swap head and tail, tail--
      condition C : head == tail --> break
```

**Code/**

```
public void evenOddChange(List<Integer> A) {
   int head = 0, tail = A.size() - 1;
   while(head < tail) {
      if(A.get(head) % 2 == 0) {
         head++;
      } else {
         Collections.swap(A, head, tail--);
      }
   }
}
```

-------------------------------- Author ------------------------------

**Thoughts/**

