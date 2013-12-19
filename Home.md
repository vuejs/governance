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
- **[Firebase Example](https://github.com/yyx990803/vue/tree/master/examples/firebase)** : a no-backend, multi-user realtime list with form validation.
- **[Component Example](https://github.com/vuejs/vue-component-example)** : an example of a highly-modular app architecture using Component as the build system.

## API Reference

### [Global Methods](wiki/Global-Methods)

- [Vue.extend(options)](wiki/Global-Methods#vueextendoptions)
- [Vue.directive(name, [directive])](wiki/Global-Methods#vuedirectivename-directive)
- [Vue.filter(name, [filter])](wiki/Global-Methods#vuefiltername-filter)
- [Vue.component(name, [component])](wiki/Global-Methods#vuecomponentname-component)
- [Vue.element(name, [element])](wiki/Global-Methods#vueelementname-element)
- [Vue.partial(name, [partial])](wiki/Global-Methods#vuepartialname-partial)
- [Vue.transition(name, [transition])](wiki/Global-Methods#vuetransitionname-transition)
- [Vue.config(options)](wiki/Global-Methods#vueconfigoptions)

### [Instantiation Options](wiki/Instantiation-Options)

- [Data & Logic](wiki/Instantiation-Options#data--logic)
    - [scope](wiki/Instantiation-Options#scope)
    - [proto](wiki/Instantiation-Options#proto)
- [DOM Element](wiki/Instantiation-Options#dom-element)
    - [el](wiki/Instantiation-Options#el)
    - [template](wiki/Instantiation-Options#template)
    - [replace](wiki/Instantiation-Options#replace)
    - [tagName](wiki/Instantiation-Options#tagname)
    - [id](wiki/Instantiation-Options#id)
    - [className](wiki/Instantiation-Options#classname)
    - [attributes](wiki/Instantiation-Options#attributes)
- [Hooks](wiki/Instantiation-Options#hooks)
    - [beforeCompile / created](wiki/Instantiation-Options#beforecompile)
    - [afterCompile / ready](wiki/Instantiation-Options#aftercompile)
    - [enteredView](wiki/Instantiation-Options#enteredview)
    - [leftView](wiki/Instantiation-Options#leftview)
    - [beforeDestroy](wiki/Instantiation-Options#beforedestroy)
    - [afterDestroy](wiki/Instantiation-Options#afterdestroy)
- [Private Assets](wiki/Instantiation-Options#private-assets)
    - [directives](wiki/Instantiation-Options#directives)
    - [filters](wiki/Instantiation-Options#filters)
    - [components](wiki/Instantiation-Options#components)
    - [elements](wiki/Instantiation-Options#elements)
    - [partials](wiki/Instantiation-Options#partials)
- [Misc](wiki/Instantiation-Options#misc)
    - [lazy](wiki/Instantiation-Options#lazy)

### [Instance Methods](wiki/Instance-Methods)

- [vm.$watch(keypath, callback)](wiki/Instance-Methods#vmwatchkeypath-callback)
- [vm.$unwatch(keypath, [callback])](wiki/Instance-Methods#vmunwatchkeypath-callback)
- [vm.$on(event, callback)](wiki/Instance-Methods#vmonevent-callback)
- [vm.$off([event, callback])](wiki/Instance-Methods#vmoffevent-callback)
- [vm.$emit(event, [args...])](wiki/Instance-Methods#vmemitevent-args)
- [vm.$broadcast(event, [args...])](wiki/Instance-Methods#vmbroadcastevent-args)
- [vm.$appendTo(element | selector)](wiki/Instance-Methods#vmappendtoelement--selector)
- [vm.$before(element | selector)](wiki/Instance-Methods#vmbeforeelement--selector)
- [vm.$after(element | selector)](wiki/Instance-Methods#vmafterelement--selector)
- [vm.$remove()](wiki/Instance-Methods#vmremove)
- [vm.$destroy()](wiki/Instance-Methods#vmdestroy)

### [Directives](wiki/Directives)

- [v-text](wiki/Directives#v-text)
- [v-html](wiki/Directives#v-html)
- [v-visible](wiki/Directives#v-visible)
- [v-show](wiki/Directives#v-show)
- [v-class](wiki/Directives#v-class)
- [v-attr](wiki/Directives#v-attr)
- [v-style](wiki/Directives#v-style)
- [v-on](wiki/Directives#v-on)
- [v-if](wiki/Directives#v-if)
- [v-repeat](wiki/Directives#v-repeat)
- [v-model](wiki/Directives#v-model)
- [v-component](wiki/Directives#v-component)
- [v-component-id](wiki/Directives#v-component-id)
- [v-transition](wiki/Directives#v-transition)
- [v-partial](wiki/Directives#v-partial)
- [v-pre](wiki/Directives#v-pre)

### [Filters](wiki/Filters)

- [capitalize](wiki/Filters#capitalize)
- [uppercase](wiki/Filters#uppercase)
- [lowercase](wiki/Filters#lowercase)
- [currency](wiki/Filters#currency)
- [pluralize](wiki/Filters#pluralize)
- [key](wiki/Filters#key)