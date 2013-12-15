# Introduction

VueJS is a MVVM library. Similar to AngularJS, VueJS uses DOM-based templates - that is, you can simply use HTML and enhance it with data-binding through directives and filters. However, VueJS is not a framework. Its goal is to provide a lighter, simpler alternative while keeping all the magical data-binding goodness.

VueJS is:

- Lightweight (10kb minified and gzipped & no dependency)
- Simple (focused on the ViewModel only)
- Modular (Nestable ViewModels & module system friendly)
- Powerful (diretives, filters, computed properties, auto dependency tracking, expressions, transitions, custom elements...)

VueJS would be particularly attractive if you:

- Like plain object models
- Like CommonJS
- Use Component as your build system

If you haven't done so yet, start with the [Getting Started Guide](wiki/Getting-Started). For example applications, check out the [TodoMVC implementation](https://github.com/yyx990803/vue/tree/master/examples/todomvc) and the [Vue + Firebase example](https://github.com/yyx990803/vue/tree/master/examples/firebase). For an example of structuring your project with Component for a highly-modular architecture, take a look at the [Vue + Component example](https://github.com/vuejs/vue-component-example).

## API Reference

### [Global Methods](wiki/Global-Methods)

- Vue.config(options)
- Vue.directive(name, [directive])
- Vue.filter(name, [filter])
- Vue.component(name, [component])
- Vue.element(name, [element])
- Vue.partial(name, [partial])
- Vue.transition(name, [transition])
- Vue.extend(options)

### [Instantiation Options](wiki/Instantiation-Options)

- Data & Logic
    - scope
- DOM Element
    - el
    - template
    - replace
    - id
    - tagName (only honored is `el` is not present)
    - className
    - attributes
- Hooks
    - init
    - teardown
- Encapsulation
    - directives
    - filters
    - components
    - elements
    - partials
- Misc
    - lazy

### [Instance Methods](wiki/Instance-Methods)

- vm.$watch(keypath, callback)
- vm.$unwatch(keypath, [callback])
- vm.$on(event, callback)
- vm.$off([event, callback])
- vm.$emit(event, [args...])
- vm.$broadcast(event, [args...])
- vm.$destroy()

### [Directives](wiki/Directives)

- v-text
- v-html
- v-visible
- v-show
- v-class
- v-attr
- v-style
- v-on
- v-if
- v-repeat
- v-model

### [Filters](wiki/Filters)

- capitalize
- uppercase
- lowercase
- currency
- pluralize
- key