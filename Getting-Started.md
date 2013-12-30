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
       }	
    }
})
```