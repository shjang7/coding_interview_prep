# must do medium questions
- [Must do Medium Questions](https://leetcode.com/list/xixy4dq7/)

- longest palindrome substring
  - [manachar algorithm](./../practice/manachar_algorithm.cpp), O(n), O(n)
  - [expand around center](./../practice/expand_around_center.rb), O(n^2), O(1)

- container with most water
  - two pointer(l, r, maxarea)
  - h[l] < h[r] ? l++ : r--
  - O(n), O(1)

- letter combinations of a phone number
  - backtracking

- generate parenthesis
  - disjoint subset
  - time and space complexity: O(4^n / √n)

- search in rotated sorted array
  - find pivot with binary search
  - find actual number with binary search
  - be careful about end point test

- permutations
  ```
  solution (input)
    backtrack(size, input, output, first)
    return output

  backtrack(size, nums, output, first)
    if (first == size)
      output.push(nums)
    for i in first ~ n
      swap(nums[first], nums[i])
      backtrack(size, nums, output, first + 1)
      swap(nums[first], nums[i])
  ```

- rotate image
  - clock wise
  - Quadrant rotation
  ```
  rotate_image(matrix)
    n = matrix.size()
    for r in 0 ~ (n+1) / 2
      for c in 0 ~ n / 2
        rotate(matrix, r, c)
  ```
  - round : (n+1) / 2
  ```
  rotate(matrix, r, c)
    n = matrix.size()
    int temp = matrix[r][c];
    matrix[r][c] = matrix[n-1-c][r];
    matrix[n-1-c][r] = matrix[n-1-r][n-1-c];
    matrix[n-1-r][n-1-c] = matrix[c][n-1-r];
    matrix[c][n-1-r] = temp;
  ```
  ```
  (r, c)
  (n-1-c, r)
  (n-1-r, n-1-c)
  (c, n-1-r)
  ```

- group anagrams
  - grouping O(n), O(n)
  ```
  vector<vector<string>> groupAnagrams(vector<string> strs)
    map<string, vector<int>> m
    for s in strs
      s.sort()
      m[s].push(index)
    vector<vector<string>> ans
    for itr in m
      vector<string> temp
      arr = itr->second
      for i in 0 ~ arr.size()
        temp.push(strs[arr[i]])
      ans.push(temp)
    return ans
  ```

- merge intervals
  - O(n log n), O(n)
  ```
  vector<vector<int>> merge(vector<vector<int>>& intervals)
    vector<vector<int>> merged
    sort(intervals)
    for interval in intervals
      if merged.empty() || merged.back()[1] < interval[0]
        merged.push(interval)
      else
        merged.back()[1] = max(merged.back()[1], interval[1])
  ```

- sort German flag colors
  - zero: 0, two: nums.size() - 1, i = 0
  - 0: swap current and next zero, zero++, i++
  - 2: swap current and next two, two--

- binary tree traversal without recursion
  - using stack

- Construct Binary Tree from Inorder and Postorder Traversal
  - traverse : postorder like preorder
  - index : using inorder with Hash-Map
  - in range : left, right

- Populating next right pointers in each node ii
  - prev, leftmost
  - prev->next = child
  - curr = curr->next

- Linked List Cycle: return the node where the cycle begins
  - phase 1: hare - tortoise algorithm
  - phase 2: one starts from meeting point, one starts from head, the meeting point equals first begin cycle
  - [proof about phase 2](./../practice/proof_of_cycle_begin.txt)

- LRU Cache
  - var: head, tail, cache
  - func: add_to_head, move_to_head, remove_node, pop_tail
  - struct: key, val, prev, next

- fraction to decimal
  - string
  - sign: +/-, abs
  - check[n] = result.length
  - result.insert(check[n], "(") << ")"

- largest number by string sort
  ```
  def comp
    order1 = a + b
    order2 = b + a
    order1 <=> order2
  end

  res = ~~~
  res[0] == '0' ? '0' : res
  ```
