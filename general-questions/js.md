# top 10 questions about js
### difference between 'let' and 'var'
  - let: es6(2015) / var: beginning: it will work for old version of browser
  - let: block scope / var: function scope
  - var: hoisted
      - declaration(선언) interpreted at beginning
      - assignment(할당) no hoisted run time\

### difference between '==' and '==='
  - '==' : compares value only ex) '1' == 1 => true
  - '===' : compares value and type ex) '1' === 1 => false

### difference between 'let' and 'const' => definition variables
  - 'let': after the first assignment we can change
  - 'const': after the first declaration, assignment we cannot reassign the value

### difference between 'null' and 'undefined' => empty
  - null: do myself, typeof(null) => object
  - undefined: original, typeof(undefined) => undefined

### use of arrow functions?
  - regular functions: 'this' indicates window object
  - arrow function: 'this' indicates current object

## JS remind
### What can node.js do?
- generate dynamic page 'content'
- CRUD: create, open, write, delete, close files on the server
