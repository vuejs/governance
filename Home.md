## Topics

- [What is VueJS?](wiki/What-is-VueJS)
- [Getting Started](wiki/Getting-Started)
- [Inline Expressions](wiki/Inline-Expressions)
- [Computed Properties](wiki/Computed-Properties)
- [Custom Directives](wiki/Custom-Directives)
- [Custom Filters](wiki/Custom-Filters)
- [Components and Elements](wiki/Components-and-Elements)
- [Transitions](wiki/Transitions)
- [Form Validation](wiki/Form-Validation)
- [Routing](wiki/Routing)

## Examples

- **[TodoMVC Implementation](https://github.com/yyx990803/vue/tree/master/examples/todomvc)** : a fully specification-compliant TodoMVC implementation in ~110 SLOC.
- [Firebase Example](https://github.com/yyx990803/vue/tree/master/examples/firebase) : a no-backend, multi-user realtime list with form validation.
- [Component Example](https://github.com/vuejs/vue-component-example) : an example of a highly-modular app architecture using Component as the build system.

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
    - proto
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