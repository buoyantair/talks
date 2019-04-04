# Notes

## ES5

### Key points

- Javascript was very loose & highly
- ES5 is released in December 2009.
- ES5 included various new features that helped javascript gain friction in
  the programming world.

### Detail

So we know that after a long long time, ES5 was released in December 2009,
in the hopes of "fixing" the language. ES5 standard was aimed to achieve the
following goals [^1]:

- Common interpretations of the language have been standardized
- New features (meta programming, accessor properties, new methods)
- Support for JSON object encoding format
- Strict Mode for more specific behaviour & unambiguous behaviour

[^1]: http://speakingjs.com/es5/ch25.html

## The Advent of NodeJS

### Key points

- NodeJS was first written in 2009
- NodeJS was becoming increasingly popular
- NodeJS accelerated the adoption of Javascript
- It is convinient to write both the serverside & the client side in Javascript

### Detail

Although NodeJS was first written in 2009, it took a while for it to get popular.
Once NodeJS started getting more and more popular, Javascript also became very popular.
Javascript's simply syntax combined with the power of NodeJS that enables developers to build
highly complex applications is very attractive.

## Versioning in Javascript: Challenges

### Key points

- The web is HUGE
- "Don't break the web"
- Fractured ecosystem
- Hard to maintain, refactor & migrate
- Developers are people

### Detail

Now we might have heard of the statement "Don't break the web". One of the challenges of
improving javascript is that each and every feature you introduce **must** be backwards compatible.
This is because almost all of the websites on the internet use Javascript one way or the other & one
single mistake can cause a huge havoc. Another risk of releasing backwards incompatible language is that
it can fracture the Javascript ecosystem. A good example of this is Python 2 & Python 3. Fractioned ecosystem
also means that developers are no longer willing to maintain, refactor and migrate a piece of software written
in older versions. So any program that was written in say older versions of javascript may not be migrated to newer
versions which means that you are missing out on a lot of cool new features! It is also tedious and very heavy on
your brain to keep track of two different language syntaxes and intricasies.

## Versioning in Javascript: The solution

### Key points

- There is no version.
- Periodically enhance the language with new features.
- Respect backwards compatiblity.
- Encourage the usage of new features over the old.
- The old features will eventually rust away & can be weeded out.

### Detail

The solution to this problem was proposed by David Herman. He proposed that there should be no versions at all!
Now how does that happen? The twist here is that we release backwards compatible features periodically every year.
This enables us to progressively enhance the language, all the while encouraging people to use the newer features
which are being introduced every year. This enables us to eventually get rid of the old & archaic language semantics
as they becoming more and more rarely used. At this point the committee that manages javascript also decided to
call each and every new release of Javascript along with the year it is released in. For example, ES2015 (ES6),
ES2016, ES2017... etc.

## TC39

### Key points

- abbrev. for "Technical Committee 39", part of ECMAInternational
- TC39 is responsible for evolving & maintaining the ECMAScript specification
- Anyone can participate

### Detail

The TC39, abbrev. for "Technical Committee 39" is responsible for developing the language specification of Javascript.
TC39 is part of ECMAInternational. The TC39 process is an open for anyone to participate. There are several stages of
rigorous testing, implementations & feedback before a proposal is accepted into the ECMAScript specification. Most
of the discussion is held in Github issues and anyone can chime in and participate. The various stages of the process
include:

- Straman (Initial idea / suggestion to the specification)
- Propsoal (More specific about the problems it solves, identifying potential challenges etc)
- Draft (Precisely describe the syntax & semantics of the feature using formal specification language)
- Candidate (Final refinement, extensive testing, feedback of the spec as well as the implementations)
- Finished (Proposal is finalised and added to the spec in the next release)

## ES5 Features

### Features

Reference: http://kangax.github.io/compat-table/es5/

#### Strict mode

Simply switch to strict mode by adding `'use strict'` at the top of the file. You can also switch to
strict mode per function by writing the same at the beginning of a function's body.

- Variables must be explicitly declared to be used & assigned to
- Functions must be declared at the top level of the scope
- Stricter rules for functions
- The arguments object has fewer properties
- this is undefined in non-method functions
- Octal literals are not allowed in strict mode.

#### Accessors

Getters & Setters enable you to get and set the properties of objects on the fly

#### Metaprogramming

Getting & Setting prototypes

- `Object.create()`
- `Object.getPrototypeOf()`

Managing attributes via property descriptors

- `Object.defineProperty()`
- `Object.defineProperties()`
- `Object.create()`
- `Object.getOwnPropertyDescriptor()`

Listing properties

- `Object.keys()`
- `Object.getOwnPropertyNames()`

Protecting objects

- `Object.preventExtensions()`
- `Object.isExtensible()`
- `Object.seal()`
- `Object.isSealed()`
- `Object.freeze()`
- `Object.isFrozen()`

New function method

- `Function.prototype.bind()`

#### New Methods

Strings

- New method `String.prototype.trim()`
- Access characters via the bracket operator [...]

New Array methods

- `Array.isArray()`
- `Array.prototype.every()`
- `Array.prototype.filter()`
- `Array.prototype.forEach()`
- `Array.prototype.indexOf()`
- `Array.prototype.lastIndexOf()`
- `Array.prototype.map()`
- `Array.prototype.reduce()`
- `Array.prototype.some()`

New Date methods:

- `Date.now()`
- `Date.prototype.toISOString()`
