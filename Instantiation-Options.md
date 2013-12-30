### Data & Logic

- #### data

    Type: `Object`

    The data object for the ViewModel. The ViewModel will proxy access to all its properties. For example, `vm.a` will return `data.a`, and `vm.a = 1` will set `data.a` to `1`. The object it self can be accessed as `vm.$data`.

- #### methods

    Type: `Object`

    Methods to be copied to the ViewModel. All methods will have their `this` context automatically bound to the ViewModel.

### DOM Element

- #### el

    Type: `String` or `HTMLElement`

- #### template

    Type: `String`

- #### replace

    Type: `Boolean`

- #### tagName
- #### id
- #### className
- #### attributes

### Lifecycle Hooks

- #### beforeCompile
**alias: created**

- #### afterCompile
**alias: ready**

- #### enteredView
- #### leftView
- #### beforeDestroy
- #### afterDestroy

### Private Assets

- #### directives
- #### filters
- #### components
- #### elements
- #### partials

### Misc

- #### lazy