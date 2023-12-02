# Symbols

Starting with ECMAScript 2015, `symbol` is a primitive data type, just
like `number` and `string`.

`symbol` values are created by calling the `Symbol` constructor.

```ts
let sym1 = Symbol();

let sym2 = Symbol("key"); // optional string key
```

Symbols are immutable, and unique.

```ts
let sym2 = Symbol("key");
let sym3 = Symbol("key");

sym2 === sym3; // false, symbols are unique
```

Just like strings, symbols can be used as keys for object properties.

```ts
const sym = Symbol();

let obj = {
  [sym]: "value",
};

console.log(obj[sym]); // "value"
```

Symbols can also be combined with computed property declarations to
declare object properties and class members.

```ts
const getClassNameSymbol = Symbol();

class C {
  [getClassNameSymbol]() {
    return "C";
  }
}

let c = new C();
let className = c[getClassNameSymbol](); // "C"
```

## `unique symbol` {#unique-symbol style="position:relative;"}

To enable treating symbols as unique literals a special type
`unique symbol` is available. `unique symbol` is a subtype of `symbol`,
and are produced only from calling `Symbol()` or `Symbol.for()`, or from
explicit type annotations. This type is only allowed on `const`
declarations and `readonly static` properties, and in order to reference
a specific unique symbol, you'll have to use the `typeof` operator. Each
reference to a unique symbol implies a completely unique identity that's
tied to a given declaration.

```ts
declare const sym1: unique symbol;
 
// sym2 can only be a constant reference.
let sym2: unique symbol = Symbol();
 
// Works - refers to a unique symbol, but its identity is tied to 'sym1'.
let sym3: typeof sym1 = sym1;
 
// Also works.
class C {
  static readonly StaticSymbol: unique symbol = Symbol();
}
```

Because each `unique symbol` has a completely separate identity, no two
`unique symbol` types are assignable or comparable to each other.

```ts
const sym2 = Symbol();
const sym3 = Symbol();
 
if (sym2 === sym3) {
  // ...
}
```

## Well-known Symbols {#well-known-symbols style="position:relative;"}

In addition to user-defined symbols, there are well-known built-in
symbols. Built-in symbols are used to represent internal language
behaviors.

Here is a list of well-known symbols:

## `Symbol.asyncIterator` {#symbolasynciterator style="position:relative;"}

A method that returns async iterator for an object, compatible to be
used with for await..of loop.

## `Symbol.hasInstance` {#symbolhasinstance style="position:relative;"}

A method that determines if a constructor object recognizes an object as
one of the constructor's instances. Called by the semantics of the
instanceof operator.

## `Symbol.isConcatSpreadable` {#symbolisconcatspreadable style="position:relative;"}

A Boolean value indicating that an object should be flattened to its
array elements by Array.prototype.concat.

## `Symbol.iterator` {#symboliterator style="position:relative;"}

A method that returns the default iterator for an object. Called by the
semantics of the for-of statement.

## `Symbol.match` {#symbolmatch style="position:relative;"}

A regular expression method that matches the regular expression against
a string. Called by the `String.prototype.match` method.

## `Symbol.replace` {#symbolreplace style="position:relative;"}

A regular expression method that replaces matched substrings of a
string. Called by the `String.prototype.replace` method.

## `Symbol.search` {#symbolsearch style="position:relative;"}

A regular expression method that returns the index within a string that
matches the regular expression. Called by the `String.prototype.search`
method.

## `Symbol.species` {#symbolspecies style="position:relative;"}

A function valued property that is the constructor function that is used
to create derived objects.

## `Symbol.split` {#symbolsplit style="position:relative;"}

A regular expression method that splits a string at the indices that
match the regular expression. Called by the `String.prototype.split`
method.

## `Symbol.toPrimitive` {#symboltoprimitive style="position:relative;"}

A method that converts an object to a corresponding primitive value.
Called by the `ToPrimitive` abstract operation.

## `Symbol.toStringTag` {#symboltostringtag style="position:relative;"}

A String value that is used in the creation of the default string
description of an object. Called by the built-in method
`Object.prototype.toString`.

## `Symbol.unscopables` {#symbolunscopables style="position:relative;"}

An Object whose own property names are property names that are excluded
from the 'with' environment bindings of the associated objects.

::: _attribution
© 2012-2023 Microsoft\
Licensed under the Apache License, Version 2.0.\
[https://www.typescriptlang.org/docs/handbook/symbols.html](https://www.typescriptlang.org/docs/handbook/symbols.html){._attribution-link}
:::
