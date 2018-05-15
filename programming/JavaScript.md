# Programming/JavaScript

## async/await

### Compose mixed with async/await and normal functions

```js
const compose = (...fns) => x =>
  fns.reduceRight(async (state, fn) =>
    Promise.resolve(fn(await state)), x)
```

[Tests](https://codepen.io/ninetails/pen/zjJZgg)
[Sauce](https://www.reddit.com/r/javascript/comments/71n1lx/using_lodash_flow_or_compose_with_asynchronous/)
