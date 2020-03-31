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
- What can node.js do?
  - generate dynamic page 'content'
  - CRUD: create, open, write, delete, close files on the server
- js mouse events: mouse events: mousedown, mouseup and click, dblclick, mousemove and finally mouseover and mouseout
- slice method in array and string
- arr.replace("hello", "world")
- arr.splice(1,2)
- const d = new Date()
- d.getFullYear()
- d.getMonth()
- Math.random()
- Math.sqrt(9)
- switch / case / default
- for (x in fruits)
- document.getElementsByTagName("p")[0]
- document.getElementsByClassName("test")[0]
- document.getElementById("demo").style.fontSize = "40px";
- element.addEventListener("click", func)
- javascript numbers are always stored as double precision floating point numbers
- The Boolean value of 0 (zero), null, undefined, empty string is false.
- The Boolean value of 0, null, undefined, empty string is false. cp) ruby - false / nil is only false
- document.getElementById(id) / document.getElementsByClassName(name) / document.getElementsByTagName(name)
- elem.innerHTML = "Hello World!";
- element.cloneNode() / document.createElement(element) / document.createTextNode(text)
- parent.removeChild(child); / parent.replaceChild(newChild, child);
- var t = setInterval(move, 10); / clearInterval(t);
- element.addEventListener("click", myFunction); / element.addEventListener("mouseover", myFunction);
- Object.assign({}, person); / Object.assign({}, person, {name: 'Bob'});
- let a, b; / ({a, b} = {a: 'Hello ', b: 'Jack'});
