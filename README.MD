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

### 3. To add any element to an array, use Array push instead of direct assignment.

