# LEETCODE-Maths-3021
```java
class Solution {
    public long flowerGame(int n, int m) {
        long EvenM = m / 2;
        long OddM = (m + 1) / 2;
        long EvenN = n / 2;
        long OddN = (n + 1) / 2;
        return EvenM * OddN + OddM * EvenN;
    }
}
```

---

### 🔎 Step-by-step Explanation

The function splits **n** and **m** into even and odd counts.

* `EvenM = m/2` → how many even numbers are there from 1 to m
* `OddM = (m+1)/2` → how many odd numbers are there from 1 to m
* `EvenN = n/2` → how many even numbers are there from 1 to n
* `OddN = (n+1)/2` → how many odd numbers are there from 1 to n

Finally:

```java
return EvenM * OddN + OddM * EvenN;
```

This is basically **#ways where one is even and the other is odd**.

---

### ✅ Dry Run Example

Suppose:

```java
n = 5, m = 4
```

1. `EvenM = m / 2 = 4 / 2 = 2` → (2, 4 are even in m)
2. `OddM = (m + 1) / 2 = (4 + 1) / 2 = 2` → (1, 3 are odd in m)
3. `EvenN = n / 2 = 5 / 2 = 2` → (2, 4 are even in n)
4. `OddN = (n + 1) / 2 = (5 + 1) / 2 = 3` → (1, 3, 5 are odd in n)

Now:

```
Result = EvenM * OddN + OddM * EvenN
       = (2 * 3) + (2 * 2)
       = 6 + 4
       = 10
```

---

### 🎯 Meaning

So `flowerGame(n, m)` returns the total **pairs (i, j)** such that:

* One number is odd and the other is even.
  (In other words, it counts mismatched parity pairs.)

---
