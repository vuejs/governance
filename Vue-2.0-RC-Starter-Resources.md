# Introduction

Exciting Times! [Vue 2.0](https://github.com/vuejs/vue/releases) is now in RC stage, and the supporting libraries – [vuex](#vuex), [vue-router](#vue-router) – and build tools – [vueify](#vueify) and [vue-loader](#vue-loader) – offer preview versions that are 2.0-ready as well! [vue-cli](#vue-cli) also offers simple templates to start hacking with `2.0` today!

While we are working on getting the docs for everything up to date, there's nothing to keep you from taking 2.0 for a test ride right now!

This collection aims to help you getting started by collecting all the information about the various libraries for 2.0 in one place.

## Vue 2.0.0-rc

### Install
```
npm install vue@next --save-dev
```

### Resources for the new API

The API of 2.0 stays mostly the same. Most changes have been under the hood (virtual DOM, anyone?), and a couple of features have been deprecated in order to make the API slimmer and more consistent and guide you to use better patterns. 

If you have never used Vue before, the best place to start is the [WIP official 2.0 Guide](http://rc.vuejs.org/guide/). The guide doesn't assume any previous Vue.js knowledge so you can jump directly into 2.0!

It's a good idea to go over the new guide even if you have previous Vue.js experience with 1.x, since there is a lot of new content thanks to the hard work by @chrisvfritz. Note the API section is not completed yet, and you can check out [this issue](https://github.com/vuejs/vuejs.org/issues/319) to keep yourself updated to the docs progress.

If you just want to know what has changed from 1.x, you can check out the [2.0 Changes Github Issue](https://github.com/vuejs/vue/issues/2873). It will offer you a quick overview of all changes, additions, and deprecations, as well as tips on how to handle the deprecations with recommended patterns (scroll past the long, awesome list of finished features and changes).

The repo's [releases page](https://github.com/vuejs/vue/releases) page offers further information as every beta/rc release comes with extensive changelogs explaining the various changes that were made.

[The examples in the `next` branch](https://github.com/vuejs/vue/tree/next/examples) are also already updated for Vue 2.0, so if you want to see some example code, this is the place to go to.

If you have any questions left (as we are sure you will), don't hesitate to ask them on http://forum.vuejs.org. Please do **not** open issues in the Github repo, as those are exclusively for bug reports, feature requests and the like.

If you find a bug, **please** don't hesitate to report it! Just follow the [Issue Reporting Guidelines](https://github.com/vuejs/vue/blob/dev/CONTRIBUTING.md#issue-reporting-guidelines).

### Standalone vs. Runtime Builds

There are two builds available, the standalone build and the runtime-only build.

- The standalone build includes the compiler and supports the `template` option.

- The runtime-only build does not include the template compiler, and does not support the `template` option. You can only use the `render` option when using the runtime-only build. The benefit is that it is roughly 1/3 lighter-weight than the standalone build.

When you use `vue-loader` or `vueify` to import `*.vue` files, their `<template>` parts are automatically compiled into `render` functions. It is therefore recommended to use the runtime-only build with `*.vue` files.

When using a bundler like Browserify or Webpack, if you do this:

``` js
import Vue from 'vue'
```

...you are getting the runtime-only build because that is the default export of the NPM package. If you do want to use the standalone build for some reason (e.g. because you have to use templates in an HTML document), you need to configure the bundler to alias `vue` to the standalone build instead.

With webpack, add the following alias to your webpack config:

```js
// ...
resolve: {
    alias: {vue: 'vue/dist/vue.js'}
},
// ....
```

For Browserify, you can use [aliasify](https://github.com/benbria/aliasify) for the same effect.

**Note: Do NOT do `import Vue from 'vue/dist/vue'` - since some tools or 3rd party libraries may import `vue` as well, this may cause the app to load both the runtime and standalone builds at the same time and lead to errors.**

## Supporting Libraries

The main support libraries are [vue-router](https://github.com/vuejs/vue-router), a router for Vue components and [vuex](https://github.com/vuejs/vuex), a reactive flux-like implementation with single-state-tree store. Both libraries are now also in 2.0-rc state, however the documentation has not been updated yet.

###  vue-router

[vue-router](https://github.com/vuejs/vue-router) is the official routing library for Vue, and it currently is in 2.0 RC state which supports Vue 2.0 and comes with several improvements and an overhauled API.

The 2.0 branch comes with [extensive examples](https://github.com/vuejs/vue-router/tree/next/examples) on how to work with the new router API.

Check the [releases page](https://github.com/vuejs/vue-router/releases) from v.2.0.0-beta.1 onwards to get detailed change lists.

**Installation**
```
npm install vue-router@next --save-dev
```

### vuex

**Two RC versions? What the heck?**

Yes, there are currently two separate Release candidates: one for version `1.0` ([Release notes](https://github.com/vuejs/vuex/releases/tag/v1.0.0-rc)) and one for Version `2.0` ([Release notes](https://github.com/vuejs/vuex/releases/tag/v2.0.0-rc.3)).

So what's the difference? 

* `v1.0.0-rc.*` essentially will be a stable release of the `<1.0.0` API. The [current docs](http://vuejs.github.io/vuex/) are already up to date for this version.
* `v2.0.0-rc.*` is a release candidate for the new API, which changed a lot. To learn about all the changes, read [this Github issue about `2.0 design`](https://github.com/vuejs/vuex/issues/236) as well as the [release notes](https://github.com/vuejs/vuex/releases) for `v2.0.0-rc.1` up to the latest version.
 
**Both Versions are compatible with Vue `1.0` *and* Vue `2.0`!!**

This is because vuex is largely independent of the changes under the hood of Vue 2.0.

**Installation**
```
# v1.0.0-rc.* is tagged as `latest` on npm so the default install will give you this version
npm install vuex --save-dev

# To install `v2.0.0-rc.*`, use the `next` tag
npm install vuex@next --save-dev
```

## Build Tools

vue-loader (for webpack) and vueify (for browserify) are already up to speed as well, offering preview versions. They will just work with Vue 2.0, there are no relevant API changes to consider.

### vue-loader

Vue 2.0 is supported from `v9.0.*` onwards. ([Release Notes](https://github.com/vuejs/vue-loader/releases))
```
npm install vue-loader@next --save-dev
```

### vueify

Pretty much the same goes for vueify - `v9.0.*` onward supports Vue 2.0. ([Release Notes](https://github.com/vuejs/vueify/releases))
```
npm install vueify@next --save-dev
```

## vue-cli and Templates

[vue-cli](https://github.com/vuejs/vuue-cli) is the command line tool that helps you to quickly set up projects with vue-loader or vueify and other goodies, like ESlint support.

vue-cli offers two flavors of templates: the 'normal' ones come with a complete setup for dev, testing and building for production, while the '-simple' versions offer a quick start to get hacking.

* The "bigger" templates (`webpack` and `browserify`) are **not** ready for vue 2.0 yet
* But there are `2.0`-ready versions of the `-simple` templates for both bundlers: [`webpack-simple-2.0`](https://github.com/vuejs-templates/webpack-simple-2.0) and [`browserify-simple-2.0`](https://github.com/vuejs-templates/browserify-simple-2.0)
````
vue init webpack-simple-2.0 my-project
vue init browserify-simple-2.0 my-project
```

Keep in mind that those are works in progress, but they should help you to get started quickly. Our goal is to have the bigger templates ready for 2.0 when the official release arrives.

If you want to upgrade the big templates for Vue 2.0 yourself, there's good news: it's not a big deal at all! We will add a small guide right here soon, so check back regularly.

## Server Side Rendering

The server-rendering functionalities are shipped in the `vue-server-renderer` package. You can check out its [documentation](https://github.com/vuejs/vue/tree/next/packages/vue-server-renderer) to get an idea of how to work with it.

## Integrated Demo

The [vue-hackernews-2.0](https://github.com/vuejs/vue-hackernews-2.0) demo is built from scratch using the latest RC versions of Vue.js, vue-router and vuex, showcasing how these libraries work seamlessly together with server-side rendering.