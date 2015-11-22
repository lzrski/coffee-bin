Compiling executables from CoffeeScript
=======================================

You may know that you can prepare command line executables for others to install with NPM. It's easy. Just add `bin` field to your `package.json` file:

```javascript
{ "bin" : { "myapp" : "./cli.js" } }
```

Here is more about it: https://docs.npmjs.com/files/package.json#bin

Now in order for this to work you need to provide a [so-called `shebang`][shebang] at the beginning of `cli.js` file, so that your shell knows how to handle it. You can't expect it to understand `javascript` on it's own. Her is how the file may look like:

```javascript
#!/usr/bin/env node

console.log("Hello, I'm bin :)");
```

Now, from the projects directory you can install it like that:

```sh
npm install --global .
```

or if you [publish it to npm repository][publish], then anybody can install it like that:

```sh
npm install --global coffee-bin
```

[publish]: https://docs.npmjs.com/getting-started/publishing-npm-packages
[shebang]: https://en.wikipedia.org/wiki/Shebang_(Unix)
