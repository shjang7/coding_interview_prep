# coding_interview_prep
- sub array sum equals k
  - O(n) time, space complexity
  - sum hashmap, range sum
  - count += map[sum - k]
  - k: 7, map[2], map[9 - 7]: 2~9

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

- sort German flag colors
  - 0: swap current and next zero
  - 2: swap current and next two

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

- sort()
  - c++
  ```
  ascending order: sort(v.begin(), v.end())
  descending order: sort(v.begin(), v.end(), greater<int>())
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
  #include <limits>
  std::numeric_limits<int>::max();
  ```

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
