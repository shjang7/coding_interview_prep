# coding_interview_prep
- sort list
  - find middle: using slow and fast pointer
  - return mergeSorting(sort(head), sort(mid));

- sort German flag colors
  - 0: swap current and next zero
  - 2: swap current and next two

- single-number
  - ruby
  ```
  arr.reduce(:^)
  ```
  - javascript
  ```
  arr.reduce((accumulator, n) => accumulator ^ n, 0)
  ```

- reduce()
  - ruby
  ```
  arr.reduce(:+)
  arr.sum()
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
