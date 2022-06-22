# ES Array
Modules [`es.array.from`](/packages/core-js/modules/es.array.from.js), [`es.array.is-array`](/packages/core-js/modules/es.array.is-array.js), [`es.array.of`](/packages/core-js/modules/es.array.of.js), [`es.array.copy-within`](/packages/core-js/modules/es.array.copy-within.js), [`es.array.fill`](/packages/core-js/modules/es.array.fill.js), [`es.array.find`](/packages/core-js/modules/es.array.find.js), [`es.array.find-index`](/packages/core-js/modules/es.array.find-index.js), [`es.array.find-last`](/packages/core-js/modules/es.array.find-last.js), [`es.array.find-last-index`](/packages/core-js/modules/es.array.find-last-index.js), [`es.array.iterator`](/packages/core-js/modules/es.array.iterator.js), [`es.array.includes`](/packages/core-js/modules/es.array.includes.js), [`es.array.push`](/packages/core-js/modules/es.array.push.js), [`es.array.slice`](/packages/core-js/modules/es.array.slice.js), [`es.array.join`](/packages/core-js/modules/es.array.join.js), [`es.array.unshift`](/packages/core-js/modules/es.array.unshift.js), [`es.array.index-of`](/packages/core-js/modules/es.array.index-of.js), [`es.array.last-index-of`](/packages/core-js/modules/es.array.last-index-of.js), [`es.array.every`](/packages/core-js/modules/es.array.every.js), [`es.array.some`](/packages/core-js/modules/es.array.some.js), [`es.array.for-each`](/packages/core-js/modules/es.array.for-each.js), [`es.array.map`](/packages/core-js/modules/es.array.map.js), [`es.array.filter`](/packages/core-js/modules/es.array.filter.js), [`es.array.reduce`](/packages/core-js/modules/es.array.reduce.js), [`es.array.reduce-right`](/packages/core-js/modules/es.array.reduce-right.js), [`es.array.reverse`](/packages/core-js/modules/es.array.reverse.js), [`es.array.sort`](/packages/core-js/modules/es.array.sort.js), [`es.array.flat`](/packages/core-js/modules/es.array.flat.js), [`es.array.flat-map`](/packages/core-js/modules/es.array.flat-map.js), [`es.array.unscopables.flat`](/packages/core-js/modules/es.array.unscopables.flat.js), [`es.array.unscopables.flat-map`](/packages/core-js/modules/es.array.unscopables.flat-map.js), [`es.array.at`](/packages/core-js/modules/es.array.at.js).
```js
class Array {
  at(index: int): any;
  concat(...args: Array<mixed>): Array<mixed>; // with adding support of @@isConcatSpreadable and @@species
  copyWithin(target: number, start: number, end?: number): this;
  entries(): Iterator<[index, value]>;
  every(callbackfn: (value: any, index: number, target: any) => boolean, thisArg?: any): boolean;
  fill(value: any, start?: number, end?: number): this;
  filter(callbackfn: (value: any, index: number, target: any) => boolean, thisArg?: any): Array<mixed>; // with adding support of @@species
  find(callbackfn: (value: any, index: number, target: any) => boolean), thisArg?: any): any;
  findIndex(callbackfn: (value: any, index: number, target: any) => boolean, thisArg?: any): uint;
  findLast(callbackfn: (value: any, index: number, target: any) => boolean, thisArg?: any): any;
  findLastIndex(callbackfn: (value: any, index: number, target: any) => boolean, thisArg?: any): uint;
  flat(depthArg?: number = 1): Array<mixed>;
  flatMap(mapFn: (value: any, index: number, target: any) => any, thisArg: any): Array<mixed>;
  forEach(callbackfn: (value: any, index: number, target: any) => void, thisArg?: any): void;
  includes(searchElement: any, from?: number): boolean;
  indexOf(searchElement: any, from?: number): number;
  join(separator: string = ','): string;
  keys(): Iterator<index>;
  lastIndexOf(searchElement: any, from?: number): number;
  map(mapFn: (value: any, index: number, target: any) => any, thisArg?: any): Array<mixed>; // with adding support of @@species
  push(...args: Array<mixed>): uint;
  reduce(callbackfn: (memo: any, value: any, index: number, target: any) => any, initialValue?: any): any;
  reduceRight(callbackfn: (memo: any, value: any, index: number, target: any) => any, initialValue?: any): any;
  reverse(): this; // Safari 12.0 bug fix
  slice(start?: number, end?: number): Array<mixed>; // with adding support of @@species
  splice(start?: number, deleteCount?: number, ...items: Array<mixed>): Array<mixed>; // with adding support of @@species
  some(callbackfn: (value: any, index: number, target: any) => boolean, thisArg?: any): boolean;
  sort(comparefn?: (a: any, b: any) => number): this; // with modern behavior like stable sort
  unshift(...args: Array<mixed>): uint;
  values(): Iterator<value>;
  @@iterator(): Iterator<value>;
  @@unscopables: { [newMethodNames: string]: true };
  static from(items: Iterable | ArrayLike, mapFn?: (value: any, index: number) => any, thisArg?: any): Array<mixed>;
  static isArray(value: any): boolean;
  static of(...args: Array<mixed>): Array<mixed>;
}

class Arguments {
  @@iterator(): Iterator<value>; // available only in core-js methods
}
```
[*CommonJS entry points:*](/docs/Usage.md#commonjs-api)
```
core-js(-pure)/es|stable|actual|full/array
core-js(-pure)/es|stable|actual|full/array/from
core-js(-pure)/es|stable|actual|full/array/of
core-js(-pure)/es|stable|actual|full/array/is-array
core-js(-pure)/es|stable|actual|full/array/at
core-js(-pure)/es|stable|actual|full/array/concat
core-js(-pure)/es|stable|actual|full/array/entries
core-js(-pure)/es|stable|actual|full/array/every
core-js(-pure)/es|stable|actual|full/array/copy-within
core-js(-pure)/es|stable|actual|full/array/fill
core-js(-pure)/es|stable|actual|full/array/filter
core-js(-pure)/es|stable|actual|full/array/find
core-js(-pure)/es|stable|actual|full/array/find-index
core-js(-pure)/es|stable|actual|full/array/find-last
core-js(-pure)/es|stable|actual|full/array/find-last-index
core-js(-pure)/es|stable|actual|full/array/flat
core-js(-pure)/es|stable|actual|full/array/flat-map
core-js(-pure)/es|stable|actual|full/array/for-each
core-js(-pure)/es|stable|actual|full/array/includes
core-js(-pure)/es|stable|actual|full/array/index-of
core-js(-pure)/es|stable|actual|full/array/iterator
core-js(-pure)/es|stable|actual|full/array/join
core-js(-pure)/es|stable|actual|full/array/keys
core-js(-pure)/es|stable|actual|full/array/last-index-of
core-js(-pure)/es|stable|actual|full/array/map
core-js(-pure)/es|stable|actual|full/array/push
core-js(-pure)/es|stable|actual|full/array/reduce
core-js(-pure)/es|stable|actual|full/array/reduce-right
core-js(-pure)/es|stable|actual|full/array/reverse
core-js(-pure)/es|stable|actual|full/array/slice
core-js(-pure)/es|stable|actual|full/array/splice
core-js(-pure)/es|stable|actual|full/array/some
core-js(-pure)/es|stable|actual|full/array/sort
core-js(-pure)/es|stable|actual|full/array/unshift
core-js(-pure)/es|stable|actual|full/array/values
core-js(-pure)/es|stable|actual|full/array/virtual/at
core-js(-pure)/es|stable|actual|full/array/virtual/concat
core-js(-pure)/es|stable|actual|full/array/virtual/copy-within
core-js(-pure)/es|stable|actual|full/array/virtual/entries
core-js(-pure)/es|stable|actual|full/array/virtual/every
core-js(-pure)/es|stable|actual|full/array/virtual/fill
core-js(-pure)/es|stable|actual|full/array/virtual/filter
core-js(-pure)/es|stable|actual|full/array/virtual/find
core-js(-pure)/es|stable|actual|full/array/virtual/find-index
core-js(-pure)/es|stable|actual|full/array/virtual/find-last
core-js(-pure)/es|stable|actual|full/array/virtual/find-last-index
core-js(-pure)/es|stable|actual|full/array/virtual/flat
core-js(-pure)/es|stable|actual|full/array/virtual/flat-map
core-js(-pure)/es|stable|actual|full/array/virtual/for-each
core-js(-pure)/es|stable|actual|full/array/virtual/includes
core-js(-pure)/es|stable|actual|full/array/virtual/index-of
core-js(-pure)/es|stable|actual|full/array/virtual/iterator
core-js(-pure)/es|stable|actual|full/array/virtual/join
core-js(-pure)/es|stable|actual|full/array/virtual/keys
core-js(-pure)/es|stable|actual|full/array/virtual/last-index-of
core-js(-pure)/es|stable|actual|full/array/virtual/map
core-js(-pure)/es|stable|actual|full/array/virtual/push
core-js(-pure)/es|stable|actual|full/array/virtual/reduce
core-js(-pure)/es|stable|actual|full/array/virtual/reduce-right
core-js(-pure)/es|stable|actual|full/array/virtual/reverse
core-js(-pure)/es|stable|actual|full/array/virtual/slice
core-js(-pure)/es|stable|actual|full/array/virtual/some
core-js(-pure)/es|stable|actual|full/array/virtual/sort
core-js(-pure)/es|stable|actual|full/array/virtual/splice
core-js(-pure)/es|stable|actual|full/array/virtual/unshift
core-js(-pure)/es|stable|actual|full/array/virtual/values
```
[*Examples*](https://tinyurl.com/2br28bgj):
```js
Array.from(new Set([1, 2, 3, 2, 1]));        // => [1, 2, 3]
Array.from({ 0: 1, 1: 2, 2: 3, length: 3 }); // => [1, 2, 3]
Array.from('123', Number);                   // => [1, 2, 3]
Array.from('123', it => it * it);            // => [1, 4, 9]

Array.of(1);       // => [1]
Array.of(1, 2, 3); // => [1, 2, 3]

let array = ['a', 'b', 'c'];

for (let value of array) console.log(value);          // => 'a', 'b', 'c'
for (let value of array.values()) console.log(value); // => 'a', 'b', 'c'
for (let key of array.keys()) console.log(key);       // => 0, 1, 2
for (let [key, value] of array.entries()) {
  console.log(key);                                   // => 0, 1, 2
  console.log(value);                                 // => 'a', 'b', 'c'
}

function isOdd(value) {
  return value % 2;
}
[4, 8, 15, 16, 23, 42].find(isOdd);      // => 15
[4, 8, 15, 16, 23, 42].findIndex(isOdd); // => 2
[1, 2, 3, 4].findLast(isOdd);            // => 3
[1, 2, 3, 4].findLastIndex(isOdd);       // => 2

Array(5).fill(42); // => [42, 42, 42, 42, 42]

[1, 2, 3, 4, 5].copyWithin(0, 3); // => [4, 5, 3, 4, 5]


[1, 2, 3].includes(2);        // => true
[1, 2, 3].includes(4);        // => false
[1, 2, 3].includes(2, 2);     // => false

[NaN].indexOf(NaN);           // => -1
[NaN].includes(NaN);          // => true
Array(1).indexOf(undefined);  // => -1
Array(1).includes(undefined); // => true

[1, [2, 3], [4, 5]].flat();    // => [1, 2, 3, 4, 5]
[1, [2, [3, [4]]], 5].flat();  // => [1, 2, [3, [4]], 5]
[1, [2, [3, [4]]], 5].flat(3); // => [1, 2, 3, 4, 5]

[{ a: 1, b: 2 }, { a: 3, b: 4 }, { a: 5, b: 6 }].flatMap(it => [it.a, it.b]); // => [1, 2, 3, 4, 5, 6]

[1, 2, 3].at(1);  // => 2
[1, 2, 3].at(-1); // => 3
```
