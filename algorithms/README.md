# algorithm questions
- Bulb switcher
  - 0: turn off all, 1: turn on all, i-th: toggle
  ```
  function bulbSwitch(n):
    if n <= 1:
      return n
    count = 1
    while count * count <= n:
      count++
    return count - 1
  ```
