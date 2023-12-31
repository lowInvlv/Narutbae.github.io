# JavaScript Environment Requirements

React 18 supports all modern browsers (Edge, Firefox, Chrome, Safari, etc).

If you support older browsers and devices such as Internet Explorer which do not provide modern browser features natively or have non-compliant implementations, consider including a global polyfill in your bundled application.

Here is a list of the modern features React 18 uses:

* [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Promise)
* [`Symbol`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Symbol)
* [`Object.assign`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Object/assign)

The correct polyfill for these features depend on your environment. For many users, you can configure your [Browserlist](https://github.com/browserslist/browserslist) settings. For others, you may need to import polyfills like [`core-js`](https://github.com/zloirock/core-js) directly.
