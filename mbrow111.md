# Profile: [Michael Brown]

- **NetID:** mbrow111
- **Major:** Data Science
- **Question that I chose from the memoization exercise:** Cutting a Rod
- **Link to the question article:** https://www.geeksforgeeks.org/cpp/initialize-a-vector-in-cpp-different-ways/
- **My solution:**

\```

    int cutRodRecursive(int rodSize, vector<int> &price, vector<int> &dp) {
        if (rodSize == 0) {
            return 0;
        }
        
        if (dp[rodSize - 1] != -1) {
            return dp[rodSize - 1]; // returned price[rodSize]
        }
        
        int ans = 0; // ans not declared and initialized
        
        for (int i = 1; i <= rodSize; i++) {
            ans = max(ans, price[i - 1] + cutRodRecursive(rodSize - i, price, dp)); // incorrect calculation
        }
        
        return dp[rodSize - 1] = ans; // No return after calculation
    }
  
    int cutRod(vector<int> &price) {
        int n = price.size();
        vector<int> dp(n, -1);
        return cutRodRecursive(n, price, dp);
    }

\```