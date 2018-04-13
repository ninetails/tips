# Programming/Node.js

## Clear console

### Reset to initial state

```js
console.reset = function () {
  return process.stdout.write('\033c');
}
```

[Source](https://gist.github.com/KenanSulayman/4990953)

### Without reset

```js
const readline = require('readline')
const blank = '\n'.repeat(process.stdout.rows)
console.log(blank)
readline.cursorTo(process.stdout, 0, 0)
readline.clearScreenDown(process.stdout)
```

[Source](https://gist.github.com/timneutkens/f2933558b8739bbf09104fb27c5c9664)
