# must do easy questions
- [Must do Easy Questions](https://leetcode.com/list/xix1yu51/)

- roman to integer
  - IV, IX, XL, XC, ... -> (-1+5), (-1+10), (-10+50), (-10+100)

- merge sorted array
  - from back to front

- linked list cycle
  - HashMap: O(n), O(n)
  - two pointers: O(m+n), O(1)

- minimum stack
  - minimum heap
  - stack

- rotate array
  - using extra space: O(n), O(n)
  - using STL rotate: O(n), O(1)
  ```
  k %= n;
  right: std::rotate(nums.begin(), nums.begin()+n-k, nums.end());
  left: std::rotate(nums.begin(), nums.begin()+k, nums.end());
  ```
  - reverse array: O(n), O(1)
  ```
  reverse(arr, 0, n-1)
  reverse(arr, 0, k-1)
  reverse(arr, k, n-1)
  ```

- happy number
  - next number: calculate each digits with squares
  - happy number: ending with 1
  - unhappy number: cycle -> recognize with HashSet

- count primes
  - Eratosthenes sieve algorithm
    ```
    prime[n]
    0, 1 -> 0
    for i -> 2 ~ sqrt(n)-1
      if prime[i]
        for j -> i*i ~ n-1, +i
          prime[j] = 0
    count = 0
    for p in prime
      if(p) count++
    count
    ```

- isomorphic
  - first -> second unique connection
  - second unique new
  - HashMap, HashSet

- invert binary tree
  - simply invert with traversing anyway

- sum of two integers without + or -
  - bit operation, recursive addition
  - a ^ b, ((unsigned int)a & b) << 1
  ```
  int getSum(int a, int b) {
      unsigned int carry = (unsigned int) a & b;
      return (b == 0) ? a : getSum(a ^ b, (int)(carry << 1));
  }
  ```

- find disappeared numbers in an array
  - the array fills from 1 to n
  - visited check with negative number
  ```
  arr[n] *= -1
  ```

- algorithm: unique binary search tree
  - Catalan number algorithm
    C(n+1) = 2(2n+1) / (n+2) * C(n)
    ```
    long long c = 1;
    for(int i = 0; i < n; i++) {
        c = c * 2*(2*i+1) / (i+2);
    }
    return (int)c;
    ```

- sub array sum equals k
  - O(n) time, space complexity
  - sum hashmap, range sum
  - count += map[sum - k]
  - k: 7, map[2], map[9 - 7]: 2~9

- subtree of another tree
  - Traverse tree
  - Check equal

- can place flowers
  - check case by case
  - checking left to right place-able
  - left should not be filled or out of range
  - right should not be filled or out of range
  - O(n), O(1)

- non decreasing array
  - decrease case should be one
  - check case by case
  - p is first or last is safe, otherwise, p-1 and p+1 or p and p+2 should be increase

- trim a binary search tree
  - recursive way
  - base case: root val in range -> not? return left recursive or right recursive
  - in range : connect left and right recursive

- longest continuous increasing subsequence
  - sliding window, O(n), O(1)

- kth largest element in a stream
  - heap sort, priority queue with greater, top

- find words that can be formed by characters
  - option 1 : copy hashmap, minus check
  - option 2 : stl string count char compare
  ```
  count(w.begin(), w.end(), c)
  ```

- trapping rain water
  - dynamic programming
  - cap left to right maximum
  - cap right to left maximum
  - each cap_minimum - height
  - exception: below 2 -> cannot trap

- three sum
  - sort
  - indexing s, l, r
  - unique: s - 1 != s, l - 1 != l, r + 1 != r

- sort list
  - find middle: using slow and fast pointer
  - return mergeSorting(sort(head), sort(mid));

- two dimensional array
  - javascript
  ```
  new Array(rLen).map(new Array(cLen));
  ```

- single-number
  - ruby
  ```
  arr.reduce(:^)
  ```
  - javascript
  ```
  arr.reduce((accumulator, n) => accumulator ^ n, 0)
  ```

- heap
  - c++
  ```
  desc: priority_queue<int, vector<int>, less<int>> pq;
  asc: priority_queue<int, vector<int>, greater<int>> pq;
  pq.push(value);
  pq.top();
  pq.pop();
  ```

- array
  - c++
  ```
  vector<int> v;
  v.resize(3);
  ```

- sort()
  - c++
  ```
  ascending order: sort(v.begin(), v.end())
  descending order: sort(v.begin(), v.end(), greater<int>())
  sort(v.begin(), v.end(), [](const int& a, const int& b){ return a > b; });
  static bool compare(const vector<int>& a, const vector<int>& b) { }
  sort(v.begin(), v.end(), compare);
  ```
  - ruby
  ```
  ascending order: arr.sort
  descending order: arr.sort { |a, b| b <=> a }
  hash.sort_by { |k, v| v }
  ```
  - javascript
  ```
  ascending order: arr.sort((a, b) => a - b)
  ```

- reduce()
  - ruby
  ```
  arr.reduce(:+)
  arr.sum()
  ```

- two dimensional array
  - javascript
  ```
  var x = new Array(10);

  for (var i = 0; i < x.length; i++) {
    x[i] = new Array(3);
  }

  console.log(x);
  ```

- max-int
  - c++
  ```
  INT_MAX
  INT_MIN
  ```
  ```
  #include <limits>
  std::numeric_limits<int>::max();
  ```

- c++ 11
  - int a{};
    - default initializer

- Stdin
  - ruby
  ```
  gets.chomp
  ```
  - c++
  ```
  std::cin
  ```
  - javascript
  ```
  const readline = require('readline');
  const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout,
    terminal: false
  });
  const data = [];
  let countOfCase = null;
  rl.on('line', function(line){
    if(countOfCase === null) {
      countOfCase = line;
    } else {
      data.push(line.split(' '));
      countOfCase -= 1;
      if (countOfCase === 0) {
        solve();
        rl.close();
      }
    }
  }
  ```
