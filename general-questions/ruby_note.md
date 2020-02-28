# Remind ruby
### [array]
- for i in (0..3)
- in loop statement, 'redo', 'retry'
- arr.insert(2, 8) -> [x,x,8,x,x]
- arr.delete_at(2)
- [1,2,3] * 3 -> [1,2,3,1,2,3,1,2,3]
- puts arr -> each element print at seperate line.
- array methods: length, sort, uniq, feeze, include?(obj), min, max

### [hash]
- hash methods: delete, key, invert, keys, values, length
- hash key can be any objects including array
- hash a.k.a. associative arrays
- hash.invert: creates hash reversing keys and values
- hash.key(value): returns key for the given value
- hash.delete(key)

### [Method]
- Methods should be defined before calling them, otherwise Ruby will raise an error.
- The actual parameter value is called an argument.
- product (multiplication)
- leave off the parentheses when using methods: more fluid reading of code
- gets.chomp is used to take user input and strip the newline at the end of the input.
- optional parameters(**p*): If you call the method without any arguments, the array p will be empty.
