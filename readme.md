# WpDevOps Elixir Browserify Support

## Step 1: Install

First ensure, that you're WpDevOps Elixir version is up to date.

```
npm install @wpdevops/elixir-browserify --save-dev
```

## Step 2: Use It

```js
// Gulpfile.js

var elixir = require('@wpdevops/elixir');

elixir(function(mix) {
    mix.browserify('main.js'); // mix.browserify(srcPath, outputPath, srcBaseDir, browserifyOptions)
});
```

This will compile, by default, `assets/js/main.js` to `dist/js/main.js`. Should you require a different source directory, either provide an optional path as the third argument to `mix.browserify`, or begin your path with `./`. This will instruct Elixir to ignore any default base directories.

```js
elixir(function(mix) {
    mix.browserify('./app/assets/js/main.js');
});
```

The same is true for the output path.

```js
elixir(function(mix) {
    mix.browserify('./app/assets/js/main.js', 'dist/build/bundle.js');
});
```

---

This package was originally ([laravel-elixir-browserify](https://github.com/JeffreyWay/laravel-elixir-browserify)) 
written by [Jeffrey Way](https://github.com/JeffreyWay)
