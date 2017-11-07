### Pass through Array

**Description/**

To get if it is possible to pass through a given array

**Variant/**

Find the minimum steps to pass through the array

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

Variant/

bottom-up DP

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



/**** Variant ****/

public int minSteps(List<Integer> steps) {
    // check is steps empty --> return 0
    int[] dp = new int[steps.size() + 1];
    for(int i = steps.size() - 1; i >= 0; i--) {
        dp[i] = Integer.MAX_VALUE;
        for(int j = 1; j <= steps.get(i) && i + j <= steps.size(); i++) {
            if(dp[i + j] != Integer.MAX_VALUE) {
                dp[i] = Math.max(dp[i], dp[i + j] + 1);
            }
        }
    }
    return dp[0];
}

```

-------------------------------- Author ------------------------------

**Thoughts/**

