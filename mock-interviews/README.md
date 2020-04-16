# mock interviews
- check-valid-string
  - "(***)": true / ")(": false
  - '(', ')', '*' => [low, high] range pattern
  - simply: low += condition ? 1 : -1
  - exception: high < 0 ? low < 0 ?
  - return: low == 0 ? low != 0 ?

- contiguous-array
     _            _    _   _
    / \          / \  / \_/
   /   \        /   \/
 _/     \_    _/
          \  /
           \/

- group anagram
  - Using hashMap, key is sorted word, value is original word grouped in array
- maximum subarray
  - divide and conquer
  - max: merge(arr, left, p), merge(arr, p, right), crossSum(arr, left, right, p)
  - crossSum: max of p.downto(left) + max of p+1.upto(right)

- longest substring
  - find / unfind case

- single num
  - bit operation, XOR, reduce

- nim game
  - find pattern 1,2,3,4,5,6, ...
  - considering like staircase problem solving

- pow(x, n)
  - fastPow,
  - n = 9 -> half = fastPow(x, 8/2)
  - half * half * x
  - n = 4 -> half = fastPow(x, 4/2)
  - half * half

- decode variations
  - dynamic programming
  ```
  function decodeVariations(S):
    N = S.length
    dp = new Array(N)
    dp[N] = 1
    for i from N-1 to 0:
        if S[i] == '0':
            dp[i] = 0
        else if S[i] == '1':
            dp[i] = dp[i+1] + dp[i+2]
        else if S[i] == '2':
            dp[i] = dp[i+1]
            if i+1 < S.length && S[i+1] <= '6':
                dp[i] += dp[i+2]
        else:
            dp[i] = dp[i+1]

    return dp[0]
  ```

- priority queue
  - meeting rooms 2: sort, priority queue greater top
