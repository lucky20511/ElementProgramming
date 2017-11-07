### Pass through Array

**Description/**

To get if it is possible to pass through a given array

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

Update the max steps for each iteration, and terminate when max steps becomes 0.

1.decrement the max steps \(move to next\)

2.update the max

3.terminate when step = 0

**Code/**

```
public boolean passArray(List<Integer> steps) {
    int maxStep = 1;
    for(int i = 0; i < steps.size(); i++) {
        maxStep = Math.max(maxStep - 1, steps.get(i));
        if(maxStep == 0) {
            return false;
        }
    }        
    return true;
}
```

-------------------------------- Author ------------------------------

**Thoughts/**

