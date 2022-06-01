# ts-levenshtein

A very efficient TS implementation calculating the Levenshtein distance, i.e. the difference between two strings. Forked from [js-levenshtein](https://github.com/gustf/js-levenshtein)

Based on Wagner-Fischer dynamic programming algorithm, optimized for speed and memory
 - use a single distance vector instead of a matrix
 - loop unrolling on the outer loop
 - remove common prefixes/postfixes from the calculation
 - minimize the number of comparisons
 - always allocate a new distance vector in order to not leak memory
 
## Install

```
$ npm install --save ts-levenshtein
```

## Usage

```ts
import levenshtein from 'ts-levenshtein';

levenshtein('kitten', 'sitting');
//=> 3
```
