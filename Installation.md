## Component

``` bash
$ component install yyx990803/vue
```
```js
var Vue = require('vue')
```

## Browserify

``` bash
$ npm install vue
```
```js
var Vue = require('vue')
```

## Bower

``` bash
$ bower install vue
```
``` html
<script src="bower_components/vue/dist/vue.js">
```
`Vue` will be registered as a global variable.

## Module Loaders

e.g. RequireJS, SeaJS: Built versions in `/dist` or installed via Bower is wrapped with UMD so it can be used directly as a CommonJS or AMD module.

## Standalone

Simply include a built version in `/dist` with a `<script>` tag.