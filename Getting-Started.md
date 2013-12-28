## Concept Overview

Concept | As in VueJS
:--- | :---
ViewModel | An object that syncs the Model and the View.
Model | A slightly modified plain JavaScript object.
View | The actual HTML that the user sees.
Directive | A prefixed HTML attribute that tells VueJS to do something about an element.
Filter | A function to process the value with before updating the View.
Expression | Simple JavaScript expressions that can be used inside directives.
Computed Property | A model property that gets auto-updated when its dependencies change.

## A Quick Example

**HTML**

``` html
<div id="demo" v-on="click:changeText">
    <p v-text="hello"></p>
</div>
```

**JavaScript**

``` js
var demo = new Vue({
    el: '#demo',
    data: {
        hello: 'Hello World!',
    },
    methods: {
    	changeText: function () {
            this.hello = 'Hello VueJS!'
       }	    }
})
```