Compiling executables from CoffeeScript
=======================================

You may know that you can prepare command line executables for others to install with NPM. It's easy. Just add `bin` field to your `package.json` file:

```javascript
{ "bin" : { "myapp" : "./cli.js" } }
```

Here is more about it: https://docs.npmjs.com/files/package.json#bin
