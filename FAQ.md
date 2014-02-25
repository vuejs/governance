- **Why doesn't Vue.js support IE8?**

    Vue.js is able to deliver the plain JavaScript object syntax without resorting to dirty checking by using `Object.defineProperty`, which is an ECMAScript 5 feature. It only works on DOM elements in IE8 and there's no way to polyfill it for JavaScript objects.

- **What is the current status of Vue.js? Can I use it in production?**

    Vue.js is currently still in beta state (as of v0.9.1), so use it with caution and check for updates often. The API and internal mechanisms will be consolidated when v0.10 lands and Vue.js will be considered suitable for production by then.

- **Where is Vue.js being used? Are there any shipped projects?**

    Vue.js is currently being used in internal projects at Google Creative Lab. Unfortunately these projects are confidential and cannot be shared with the public at this moment. However you are welcome to submit anything you built with Vue.js! Just send a tweet to @vuejs.

- **So is Vue.js a Google project?**

    No. Although it is being used at Google Creative Lab, Vue.js is a personal project and fully open sourced under the MIT License.

- **What is the difference between Vue.js and AngularJS?**

    There are a few reasons to use Vue over Angular, although they might not apply for everyone:

    1. Vue.js is a more flexible, less opinionated solution. That allows you to structure your app the way you want it to be, instead of being forced to do everything the Angular way. It's only an interface layer so you can use it as a light feature in pages instead of a full blown SPA. It gives you bigger room to mix and match with other libraries. This is probably the most important distinction.

    2. Vue.js is much simpler than Angular in general, so you can learn almost everything about it really fast and get productive.

    3. Vue.js has better performance because it doesn't use dirty checking. Angular gets slow when there are a lot of watchers, because every time anything in the scope changes, all these watchers need to be re-evaluated again. Vue.js doesn't suffer from this because under it uses an event based observing mechanism, so all changes trigger independently unless they have explicit dependency relationships.

    4. Vue.js has a clearer separation between directives and components. Directives are meant to encapsulate DOM manipulations only, while Components stand for a self-contained unit that has its own view and data logic. In Angular there's a lot of confusion between the two.

    But also note:

    1. Vue.js is a relatively young project and is not fully stable yet, while Angular is battle-proven and has a larger community. So if you want something for a large, serious production app you might want to pick Angular.

    2. Vue.js only supports IE9 and above while Angular suppots IE8.

- **What is the future plan?**

    See the [Roadmap](https://github.com/yyx990803/vue/issues/78).