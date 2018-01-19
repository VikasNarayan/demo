# React - Basic Theoretical Concepts

This document is my attempt to formally explain my mental model of React. The intention is to describe this in terms of deductive reasoning that lead us to this design.

There may certainly be some premises that are debatable and the actual design of this example may have bugs and gaps. This is just the beginning of formalizing it. Feel free to send a pull request if you have a better idea of how to formalize it. The progression from simple -> complex should make sense along the way without too many library details shining through.

The actual implementation of React.js is full of pragmatic solutions, incremental steps, algorithmic optimizations, legacy code, debug tooling and things you need to make it actually useful. Those things are more fleeting, can change over time if it is valuable enough and have high enough priority. The actual implementation is much more difficult to reason about.

I like to have a simpler mental model that I can ground myself in.

## Transformation

The core premise for React is that UIs are simply a projection of data into a different form of data. The same input gives the same output. A simple pure function.

```js
function NameBox(name) {
  return { fontWeight: 'bold', labelContent: name };
}
```

```
'Sebastian Markbåge' ->
{ fontWeight: 'bold', labelContent: 'Sebastian Markbåge' };
```
