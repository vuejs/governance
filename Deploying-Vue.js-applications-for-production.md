The minified standalone build of Vue.js has already stripped out all the warnings for you for a smaller file size, but when you are using tools like Browserify for Webpack to build Vue.js applications, it's not so obvious how to do that.

Starting in 0.12.8, it is quite simple to configure the tools to strip out the warnings:

### Webpack

Use Webpack's `DefinePlugin` to indicate a production environment, so that warning blocks can be automatically dropped by UglifyJS during minification. Example config:

``` js
var webpack = require('webpack')

module.exports = {
  // ...
  plugins: [
    // ...
    new webpack.DefinePlugin({
      'process.env': {
        NODE_ENV: '"production"'
      }
    }),
    new webpack.optimize.UglifyJsPlugin({
      compress: {
        warnings: false
      }
    })
  ]
}
```

### Browserify

Just run your bundling command with `NODE_ENV` set to `"production"`. Vue automatically applies `envify` transform to itself and makes warning blocks unreachable.