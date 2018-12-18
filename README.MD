# JavaScript Top 10 Rules Guide

## 1. Naming

	Identifiers use only letters and digits, and, in a small number of cases noted below, underscores and very rarely (when required by frameworks like Angular) dollar signs.

	Give as descriptive a name as possible, within reason. Do not worry about saving horizontal space as it is far more important to make your code immediately understandable by a new reader. Do not use abbreviations that are ambiguous or unfamiliar to readers outside your project, and do not abbreviate by deleting letters within a word.
		
```js
priceCountReader      // No abbreviation.
numErrors             // "num" is a widespread convention.
numDnsConnections     // Most people know what "DNS" stands for.
```

Illegal:

```js
n                     // Meaningless.
nErr                  // Ambiguous abbreviation.
nCompConns            // Ambiguous abbreviation.
wgcConnections        // Only your group knows what this stands for.
pcReader              // Lots of things can be abbreviated "pc".
cstmrId               // Deletes internal letters.
kSecondsPerDay        // Do not use Hungarian notation.
```

## 2. No more than one space is used for indents of keywords, operators, etc.

Illegal:

```js 
var name       = "andrei";
var sureName = "corcinschi";
```

Good way:

```js
var name = "andrei";
var sureName = "corcinschi";
```

## 3. Use abbreviated object properties.

Illegal:

```js
const johnSmith = 'John Smith';
const obj = {
  johnSmith: johnSmith,
};
```

Good way:

```js
const johnSmith = 'John Smith';
const obj = {
  johnSmith,
};
```

### 4. To add any element to an array, use Array push instead of direct assignment. 

Illegal:

```js
const someStack = [];

someStack[someStack.length] = 'hello';
```

Good way:
```js
const someStack = [];

someStack.push('hello');
```

### 5. To copy arrays use spread ...

Illegal:

```js
const len = items.length;
const itemsCopy = [];
let i;

for (i = 0; i < len; i += 1) {
  itemsCopy[i] = items[i];
}
```

Good way:

```js
const itemsCopy = [...items];
```

### 5. Use single quotes for strings.

Illegal:

```js
const name = "Capt. Janeway";

// BAD - a pattern string literal must contain interpolation or line breaks
const name = `Capt. Janeway`;
```

Good way:

```js
const name = 'Capt. Janeway';
```

### 6. Use literal notation to create an array.

Illegal:

```js
const items = new Array();
```

Good way:

```js
const items = [];
```

### 7. Use literal notation to create an object.

const items = new Object();
```

Good way:

```js
const items = {};
```

### 8. If you need to override values, use let instead of var

Illegal:

```js
var count = 1;
if (true) {
  count += 1;
}
```

Good way:

```js
let count = 1;
if (true) {
  count += 1;
}
```

### 9. The opening brackets of code blocks are on the same line with the operator that they are used by

Illegal:

```js
if (condition)
{
  // ...
}
```

Good way:

```js
if (condition) {
  // ...
}
```

### 10. Use const to declare variables, avoid var

Illegal:

```js
var a = 1;
var b = 2;
```

Good way:

```js
const a = 1;
const b = 2;
```