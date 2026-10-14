# Profile: [Your Full Name]

- **NetID:** aryasp2
- **Major:** Computer Science with a concentration in Software Engineering
- **Question that I chose from the memoization exercise:** Count ways to reach the n'th stair.
- **Link to the question article:** https://www.geeksforgeeks.org/problems/count-ways-to-reach-the-nth-stair-1587115620/1
- **My solution:**

\```

#include <stdio.h>

int climbStairs(int n) {
    if (n <= 1) return 1;
    if (n == 2) return 2; // remember if there are 2 stairs, there are 2 ways to climb: (1+1) or (2)
    return climbStairs(n - 1) + climbStairs(n - 2);
}

int main() {
    int n = 5;
    printf("Number of ways to climb %d stairs: %d\n", n, climbStairs(n));
}

\```
