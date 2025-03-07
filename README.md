![logo](https://user-images.githubusercontent.com/2213682/146607186-8e13ddef-26a4-4ebf-befd-5aac9d77c090.png)

<div align=center>

[![fundraising](https://opencollective.com/core-js/all/badge.svg?label=fundraising)](https://opencollective.com/core-js) [![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/zloirock/core-js/blob/master/CONTRIBUTING.md) [![version](https://img.shields.io/npm/v/core-js.svg)](https://www.npmjs.com/package/core-js) [![core-js downloads](https://img.shields.io/npm/dm/core-js.svg?label=npm%20i%20core-js)](https://npm-stat.com/charts.html?package=core-js&package=core-js-pure&package=core-js-compat&from=2014-11-18) [![core-js-pure downloads](https://img.shields.io/npm/dm/core-js-pure.svg?label=npm%20i%20core-js-pure)](https://npm-stat.com/charts.html?package=core-js&package=core-js-pure&package=core-js-compat&from=2014-11-18) [![jsDelivr](https://data.jsdelivr.com/v1/package/npm/core-js-bundle/badge?style=rounded)](https://www.jsdelivr.com/package/npm/core-js-bundle) [![tests](https://github.com/zloirock/core-js/workflows/tests/badge.svg)](https://github.com/zloirock/core-js/actions) [![eslint](https://github.com/zloirock/core-js/workflows/eslint/badge.svg)](https://github.com/zloirock/core-js/actions)

</div>

> Modular standard library for JavaScript. Includes polyfills for [ECMAScript up to 2023](docs/features/ecmascript/README.md): [promises](docs/features/ecmascript/Promise.md), [symbols](docs/features/ecmascript/symbol.md), [collections](docs/features/ecmascript/collections.md), iterators, [typed arrays](docs/features/ecmascript/typed-array.md), many other features, [ECMAScript proposals](docs/features/proposals/README.md), [some cross-platform WHATWG / W3C features and proposals](docs/features/web-standards/README.md) like [`URL`](docs/features/web-standards/url.md). You can load only required features or use it without global namespace pollution.

**If you are looking for documentation for obsolete `core-js@2`, please, check [this branch](https://github.com/zloirock/core-js/tree/v2).**

## As advertising: the author is looking for a good job -)

## [core-js@3, babel and a look into the future](docs/2019-03-19-core-js-3-babel-and-a-look-into-the-future.md)

## Raising funds

`core-js` isn't backed by a company, so the future of this project depends on you. Become a sponsor or a backer if you are interested in `core-js`: [**Open Collective**](https://opencollective.com/core-js), [**Patreon**](https://patreon.com/zloirock), **Bitcoin ( bc1qlea7544qtsmj2rayg0lthvza9fau63ux0fstcz )**.

---

<a href="https://opencollective.com/core-js/sponsor/0/website" target="_blank"><img src="https://opencollective.com/core-js/sponsor/0/avatar.svg"></a><a href="https://opencollective.com/core-js/sponsor/1/website" target="_blank"><img src="https://opencollective.com/core-js/sponsor/1/avatar.svg"></a><a href="https://opencollective.com/core-js/sponsor/2/website" target="_blank"><img src="https://opencollective.com/core-js/sponsor/2/avatar.svg"></a><a href="https://opencollective.com/core-js/sponsor/3/website" target="_blank"><img src="https://opencollective.com/core-js/sponsor/3/avatar.svg"></a><a href="https://opencollective.com/core-js/sponsor/4/website" target="_blank"><img src="https://opencollective.com/core-js/sponsor/4/avatar.svg"></a><a href="https://opencollective.com/core-js/sponsor/5/website" target="_blank"><img src="https://opencollective.com/core-js/sponsor/5/avatar.svg"></a><a href="https://opencollective.com/core-js/sponsor/6/website" target="_blank"><img src="https://opencollective.com/core-js/sponsor/6/avatar.svg"></a><a href="https://opencollective.com/core-js/sponsor/7/website" target="_blank"><img src="https://opencollective.com/core-js/sponsor/7/avatar.svg"></a><a href="https://opencollective.com/core-js/sponsor/8/website" target="_blank"><img src="https://opencollective.com/core-js/sponsor/8/avatar.svg"></a><a href="https://opencollective.com/core-js/sponsor/9/website" target="_blank"><img src="https://opencollective.com/core-js/sponsor/9/avatar.svg"></a><a href="https://opencollective.com/core-js/sponsor/10/website" target="_blank"><img src="https://opencollective.com/core-js/sponsor/10/avatar.svg"></a><a href="https://opencollective.com/core-js/sponsor/11/website" target="_blank"><img src="https://opencollective.com/core-js/sponsor/11/avatar.svg"></a>

---

<a href="https://opencollective.com/core-js#backers" target="_blank"><img src="https://opencollective.com/core-js/backers.svg?width=890"></a>

---

# Example
[*Example of usage*](https://tinyurl.com/2aj9lkwf):
```js
import 'core-js/actual'; // <- at the top of your entry point

Array.from(new Set([1, 2, 3, 2, 1]));          // => [1, 2, 3]
[1, 2, 3, 4, 5].group(it => it % 2);           // => { 1: [1, 3, 5], 0: [2, 4] }
Promise.resolve(42).then(x => console.log(x)); // => 42
structuredClone(new Set([1, 2, 3]));           // => new Set([1, 2, 3])
queueMicrotask(() => console.log('called as microtask'));
```

*You can load only required features*:
```js
import 'core-js/actual/array/from';       // <- at the top of your entry point
import 'core-js/actual/array/group';      // <- at the top of your entry point
import 'core-js/actual/set';              // <- at the top of your entry point
import 'core-js/actual/promise';          // <- at the top of your entry point
import 'core-js/actual/structured-clone'; // <- at the top of your entry point
import 'core-js/actual/queue-microtask';  // <- at the top of your entry point

Array.from(new Set([1, 2, 3, 2, 1]));          // => [1, 2, 3]
[1, 2, 3, 4, 5].group(it => it % 2);           // => { 1: [1, 3, 5], 0: [2, 4] }
Promise.resolve(42).then(x => console.log(x)); // => 42
structuredClone(new Set([1, 2, 3]));           // => new Set([1, 2, 3])
queueMicrotask(() => console.log('called as microtask'));
```

*Or use it without global namespace pollution*:
```js
import from from 'core-js-pure/actual/array/from';
import group from 'core-js-pure/actual/array/group';
import Set from 'core-js-pure/actual/set';
import Promise from 'core-js-pure/actual/promise';
import structuredClone from 'core-js-pure/actual/structured-clone';
import queueMicrotask from 'core-js-pure/actual/queue-microtask';

from(new Set([1, 2, 3, 2, 1]));                // => [1, 2, 3]
group([1, 2, 3, 4, 5], it => it % 2);          // => { 1: [1, 3, 5], 0: [2, 4] }
Promise.resolve(42).then(x => console.log(x)); // => 42
structuredClone(new Set([1, 2, 3]));           // => new Set([1, 2, 3])
queueMicrotask(() => console.log('called as microtask'));
```

## [Index](docs)
- [Usage](docs/usage.md)
  - [Installation](docs/usage.md#installation)
  - [`postinstall` message](docs/usage.md#postinstall-message)
  - [CommonJS API](/docs/usage.md#commonjs-api)
  - [Babel](docs/usage.md#babel)
    - [`@babel/polyfill`](docs/usage.md#babelpolyfill)
    - [`@babel/preset-env`](docs/usage.md#babelpreset-env)
    - [`@babel/runtime`](docs/usage.md#babelruntime)
  - [swc](docs/usage.md#swc)
  - [Configurable level of aggressiveness](docs/usage.md#configurable-level-of-aggressiveness)
  - [Custom build](docs/usage.md#custom-build)
- [Compatibility data](docs/compatibility-data.md)
- [Supported engines](docs/compatibility-data.md#supported-engines)
- [Features](docs/features/README.md)
  - [ECMAScript](docs/features/ecmascript/README.md)
    - [ECMAScript: Object](docs/features/ecmascript/object.md)
    - [ECMAScript: Function](docs/features/ecmascript/function.md)
    - [ECMAScript: Error](docs/features/ecmascript/error.md)
    - [ECMAScript: Array](docs/features/ecmascript/array.md)
    - [ECMAScript: String and RegExp](docs/features/ecmascript/string%20and%20regexp.md)
    - [ECMAScript: Number](docs/features/ecmascript/number.md)
    - [ECMAScript: Math](docs/features/ecmascript/math.md)
    - [ECMAScript: Date](docs/features/ecmascript/date.md)
    - [ECMAScript: Promise](docs/features/ecmascript/promise.md)
    - [ECMAScript: Symbol](docs/features/ecmascript/symbol.md)
    - [ECMAScript: Collections](docs/features/ecmascript/collections.md)
    - [ECMAScript: Typed Arrays](docs/features/ecmascript/typed-array.md)
    - [ECMAScript: Reflect](docs/features/ecmascript/reflect.md)
    - [ECMAScript: JSON](docs/features/ecmascript/json.md)
    - [ECMAScript: globalThis](docs/features/ecmascript/global-this.md)
  - [ECMAScript proposals](docs/features/proposals/README.md)
    - [Finished proposals](docs/features/proposals#finished)
      - [`globalThis`](docs/features/proposals/global-this.md)
      - [Relative indexing method](docs/features/proposals/relative-indexing-method.md)
      - [`Array.prototype.includes`](docs/features/proposals/array-includes.md)
      - [`Array.prototype.flat` / `Array.prototype.flatMap`](docs/features/proposals/array-flat-map.md)
      - [`Array` find from last](docs/features/proposals/array-find-from-last.md)
      - [`Object.values` / `Object.entries`](docs/features/proposals/object-values-entries.md)
      - [`Object.fromEntries`](docs/features/proposals/object-from-entries.md)
      - [`Object.getOwnPropertyDescriptors`](docs/features/proposals/object-getownpropertydescriptors.md)
      - [Accessible `Object.prototype.hasOwnProperty`](docs/features/proposals/accessible-object-hasownproperty.md)
      - [`String` padding](docs/features/proposals/string-padding.md)
      - [`String.prototype.matchAll`](docs/features/proposals/string-match-all.md)
      - [`String.prototype.replaceAll`](docs/features/proposals/string-replace-all.md)
      - [`String.prototype.trimStart` / `String.prototype.trimEnd`](docs/features/proposals/string-left-right-trim.md)
      - [`RegExp` `s` (`dotAll`) flag](docs/features/proposals/regexp-dotall-flag.md)
      - [`RegExp` named capture groups](docs/features/proposals/regexp-named-groups.md)
      - [`Promise.allSettled`](docs/features/proposals/promise-all-settled.md)
      - [`Promise.any`](docs/features/proposals/promise-any.md)
      - [`Promise.prototype.finally`](docs/features/proposals/promise-finally.md)
      - [`Symbol.asyncIterator` for asynchronous iteration](docs/features/proposals/async-iteration.md)
      - [`Symbol.prototype.description`](docs/features/proposals/symbol-description.md)
      - [Well-formed `JSON.stringify`](docs/features/proposals/well-formed-stringify.md)
    - [Stage 3 proposals](docs/features/proposals#stage-3)
      - [`Array` grouping](docs/features/proposals/array-grouping.md)
      - [Change `Array` by copy](docs/features/proposals/change-array-by-copy.md)
    - [Stage 2 proposals](docs/features/proposals#stage-2)
      - [`Iterator` helpers](docs/features/proposals/iterator-helpers.md)
      - [New `Set` methods](docs/features/proposals/set-methods.md)
      - [`Map.prototype.emplace`](docs/features/proposals/map-upsert.md)
      - [`Array.fromAsync`](docs/features/proposals/array-from-async.md)
      - [`Array.isTemplateObject`](docs/features/proposals/array-is-template-object.md)
      - [`Symbol.{ asyncDispose, dispose }` for `using` statement](docs/features/proposals/using-statement.md)
      - [`Symbol.metadataKey` for decorators metadata proposal](docs/features/proposals/decorator-metadata.md)
    - [Stage 1 proposals](docs/features/proposals#stage-1)
      - [`Observable`](docs/features/proposals/observable.md)
      - [New collections methods](docs/features/proposals/collection-methods.md)
      - [`.of` and `.from` methods on collection constructors](docs/features/proposals/collection-of-from.md)
      - [`compositeKey` and `compositeSymbol`](docs/features/proposals/keys-composition.md)
      - [`Array` filtering](docs/features/proposals/array-filtering.md)
      - [`Array` deduplication](docs/features/proposals/array-unique.md)
      - [Getting last item from `Array`](docs/features/proposals/array-find-from-last.md)
      - [`Number.range`](docs/features/proposals/number-range.md)
      - [`Number.fromString`](docs/features/proposals/number-from-string.md)
      - [`Math` extensions](docs/features/proposals/math-extensions.md)
      - [`Math.signbit`](docs/features/proposals/math-signbit.md)
      - [`String.cooked`](docs/features/proposals/string-cooked.md)
      - [`String.prototype.codePoints`](docs/features/proposals/string-code-points.md)
      - [`Symbol.matcher` for pattern matching](docs/features/proposals/pattern-matching.md)
    - [Stage 0 proposals](docs/features/proposals#stage-0)
      - [`Function.prototype.unThis`](docs/features/proposals/function-un-this.md)
      - [`Function.{ isCallable, isConstructor }`](docs/features/proposals/function-is-callable-is-constructor.md)
      - [`URL`](docs/features/proposals/url.md)
    - [Pre-stage 0 proposals](docs/features/proposals#pre-stage-0)
      - [`Reflect` metadata](docs/features/proposals/reflect-metadata.md)
  - [Web standards](docs/features/web-standards/README.md)
    - [`structuredClone`](docs/features/web-standards/structured-clone.md)
    - [Base64 utility methods](docs/features/web-standards/base64-utility-methods.md)
    - [`setTimeout` and `setInterval`](docs/features/web-standards/set-timeout%20and%20set-interval.md)
    - [`setImmediate`](docs/features/web-standards/set-immediate.md)
    - [`queueMicrotask`](docs/features/web-standards/queue-microtask.md)
    - [`URL` and `URLSearchParams`](docs/features/web-standards/url.md)
    - [`DOMException`](docs/features/web-standards/dom-exception.md)
    - [Iterable DOM collections](docs/features/web-standards/dom-collections.md)
  - [Iteration helpers](docs/features/iteration-helpers.md)
- [Missing polyfills](docs/missing-polyfills.md)
- [Contributing](CONTRIBUTING.md)
- [Security policy](SECURITY.md)
- [Changelog](CHANGELOG.md)

### [Usage](docs/usage.md)
#### [Installation:](docs/usage.md#installation)
#### [`postinstall` message](docs/usage.md#postinstall-message)
#### [CommonJS API](docs/usage.md#commonjs-api)
##### [Caveats when using CommonJS API](docs/usage.md#caveats-when-using-commonjs-api)
##### [CommonJS and prototype methods without global namespace pollution](docs/usage.md#commonjs-and-prototype-methods-without-global-namespace-pollution)
#### [Babel](docs/usage.md#babel)
##### [`@babel/polyfill`](docs/usage.md#babelpolyfill)
##### [`@babel/preset-env`](docs/usage.md#babelpreset-env)
##### [`@babel/runtime`](docs/usage.md#babelruntime)
#### [swc](docs/usage.md#swc)
#### [Configurable level of aggressiveness](docs/usage.md#configurable-level-of-aggressiveness)
#### [Custom build](docs/usage.md#custom-build)

### [Compatibility data](docs/compatibility-data.md)

### [Supported engines](docs/compatibility-data.md#supported-engines)

### [Features:](docs/features/README.md)

#### [ECMAScript](docs/features/ecmascript/README.md)
##### [ECMAScript: Object](docs/features/ecmascript/object.md)
##### [ECMAScript: Function](docs/features/ecmascript/function.md)
##### [ECMAScript: Error](docs/features/ecmascript/error.md)
##### [ECMAScript: Array](docs/features/ecmascript/array.md)
##### [ECMAScript: String and RegExp](docs/features/ecmascript/string%20and%20regexp.md)
##### [ECMAScript: Number](docs/features/ecmascript/number.md)
##### [ECMAScript: Math](docs/features/ecmascript/math.md)
##### [ECMAScript: Date](docs/features/ecmascript/date.md)
##### [ECMAScript: Promise](docs/features/ecmascript/promise.md)
###### [Unhandled rejection tracking](docs/features/ecmascript/promise.md#unhandled-rejection-tracking)
##### [ECMAScript: Symbol](docs/features/ecmascript/symbol.md)
###### [Caveats when using `Symbol` polyfill](docs/features/ecmascript/symbol.md#caveats-when-using-symbol-polyfill)
##### [ECMAScript: Collections](docs/features/ecmascript/collections.md)
###### [Map](docs/features/ecmascript/collections.mp#map)
###### [Set](docs/features/ecmascript/collections.md#set)
###### [WeakMap](docs/features/ecmascript/collections#weakmap)
###### [WeakSet](docs/features/ecmascript/collections#weakset)
###### [Caveats when using collections polyfill](docs/features/ecmascript/collections.md#caveats-when-using-collections-polyfill)

##### [ECMAScript: Typed Arrays](docs/features/ecmascript/typed-array.md)
###### [Caveats when using typed arrays polyfills](docs/features/ecmascript/typed-array.md#caveats-when-using-typed-arrays-polyfills)
##### [ECMAScript: Reflect](docs/features/ecmascript/reflect.md)
##### [ECMAScript: JSON](docs/features/ecmascript/json.md)
##### [ECMAScript: globalThis](docs/features/ecmascript/global-this.md)

#### [ECMAScript proposals](docs/features/proposals/README.md)
##### [Finished proposals](docs/features/proposals/README.md#finished)
###### [`globalThis`](docs/features/proposals/global-this.md)
###### [Relative indexing method](docs/features/proposals/relative-indexing-method.md)
###### [`Array.prototype.includes`](docs/features/proposals/array-includes.md)
###### [`Array.prototype.flat` / `Array.prototype.flatMap`](docs/features/proposals/array-flat-map.md)
###### [Array find from last](docs/features/proposals/array-find-from-last.md)
###### [`Object.values` / `Object.entries`](docs/features/proposals/object-values-entries.md)
###### [`Object.fromEntries`](docs/features/proposals/object-from-entries.md)
###### [`Object.getOwnPropertyDescriptors`](docs/features/proposals/object-getownpropertydescriptors.md)
###### [Accessible `Object.prototype.hasOwnProperty`](docs/features/proposals/accessible-object-hasownproperty.md)
###### [`String` padding](docs/features/proposals/string-padding.md)
###### [`String#matchAll`](docs/features/proposals/string-match-all.md)
###### [`String#replaceAll`](docs/features/proposals/string-replace-all.md)
###### [`String.prototype.trimStart` / `String.prototype.trimEnd`](docs/features/proposals/string-left-right-trim.md)
###### [`RegExp` `s` (`dotAll`) flag](docs/features/proposals/regexp-dotall-flag.md)
###### [`RegExp` named capture groups](docs/features/proposals/regexp-named-groups.md)
###### [`Promise.allSettled`](docs/features/proposals/promise-all-settled.md)
###### [`Promise.any`](docs/features/proposals/promise-any.md)
###### [`Promise.prototype.finally`](docs/features/proposals/promise-finally.md)
###### [`Symbol.asyncIterator` for asynchronous iteration](docs/features/proposals/async-iteration.md)
###### [`Symbol.prototype.description`](docs/features/proposals/symbol-description.md)
###### [Well-formed `JSON.stringify`](docs/features/proposals/well-formed-stringify.md)

##### [Stage 3 proposals](docs/features/proposals/README.md#stage-3)
###### [`Array` grouping](docs/features/proposals/array-grouping.md)
###### [Change `Array` by copy](docs/features/proposals/change-array-by-copy.md)

##### [Stage 2 proposals](docs/features/proposals/README.md#stage-2)
###### [Iterator helpers](docs/features/proposals/iterator-helpers.md)
- [Caveats](docs/features/proposals/iterator-helpers.md#caveats)
###### [New `Set` methods](docs/features/proposals/set-methods.md)
###### [`Map.prototype.emplace`](docs/features/proposals/map-upsert.md)
###### [`Array.fromAsync`](docs/features/proposals/array-from-async.md)
###### [`Array.isTemplateObject`](docs/features/proposals/array-is-template-object.md)
###### [`Symbol.{ asyncDispose, dispose }` for `using` statement](docs/features/proposals/using-statement.md)
###### [`Symbol.metadataKey` for decorators metadata proposal](docs/features/proposals/decorator-metadata.md)

##### [Stage 1 proposals](docs/features/proposals/README.md#stage-1)
###### [`Observable`](docs/features/proposals/observable.md)
###### [New collections methods](docs/features/proposals/collection-methods.md)
###### [`.of` and `.from` methods on collection constructors](docs/features/proposals/collection-of-from.md)
###### [`compositeKey` and `compositeSymbol`](docs/features/proposals/keys-composition.md)
###### [Array filtering](docs/features/proposals/array-filtering.md)
###### [Array deduplication](docs/features/proposals/array-unique.md)
###### [Getting last item from `Array`](docs/features/proposals/array-find-from-last.md)
###### [`Number.range`](docs/features/proposals/number-range.md)
###### [`Number.fromString`](docs/features/proposals/number-from-string.md)
###### [`Math` extensions](docs/features/proposals/math-extensions.md)
###### [`Math.signbit`](docs/features/proposals/math-signbit.md)
###### [`String.cooked`](docs/features/proposals/string-cooked.md)
###### [`String.prototype.codePoints`](docs/features/proposals/string-code-points.md)
###### [`Symbol.matcher` for pattern matching](docs/features/proposals/pattern-matching.md)
###### [Seeded pseudo-random numbers](docs/features/proposals/seeded-random.md)
###### [Object iteration](docs/features/proposals/object-iteration.md)
###### [`Promise.try`](docs/features/proposals/promise-try.md)

##### [Stage 0 proposals](docs/features/proposals/README.md#stage-0)
###### [`Function.prototype.unThis`](docs/features/proposals/function-un-this.md)
###### [`Function.{ isCallable, isConstructor }`](docs/features/proposals/function-is-callable-is-constructor.md)
###### [`URL`](docs/features/proposals/url.md)
###### [`String#at`](docs/features/proposals/string-at.md)
###### [Efficient 64 bit arithmetic](docs/features/proposals/efficient-64-bit-arithmetic.md)

##### [Pre-stage 0 proposals](docs/features/proposals/README.md#pre-stage-0)
###### [`Reflect` metadata](docs/features/proposals/reflect-metadata.md)


#### [Web standards](docs/features/web-standards/README.md)
##### [`structuredClone`](docs/features/web-standards/structuredclone)
###### [Caveats when using `structuredClone` polyfill](docs/features/web-standards/structured-clone.md#caveats-when-using-structuredclone-polyfill)
##### [Base64 utility methods](docs/features/web-standards/base64-utility-methods.md)
##### [`setTimeout` and `setInterval`](docs/features/web-standards/set-timeout%20and%20set-interval.md)
##### [`setImmediate`](docs/features/web-standards/set-immediate.md)
##### [`QueueMicrotask`](docs/features/web-standards/queue-microtask.md)
##### [`URL` and `URLSearchParams`](docs/features/web-standards/url.md)
###### [Caveats when using `URL` and `URLSearchParams`](docs/features/web-standards/url.md#caveats-when-using-url-and-urlsearchparams)
##### [`DOMException`](docs/features/web-standards/dom-exception.md)
##### [Iterable DOM collections](docs/features/web-standards/dom-collections.md)

#### [Iteration helpers](docs/features/iteration-helpers.md)

### [Missing polyfills](docs/missing-polyfills.md)
