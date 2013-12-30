VueJS is a library that aims to simplify the development of interactive interfaces.

Technically, it provides the **[ViewModel]** layer of the MVVM pattern, which connects the **[View]** (the actual HTML that the user sees) and the **[Model]** (JSON-compliant plain JavaScript objects) via two way data-bindings.

Philosophically, the goal is to allow the developer to embrace an extremely minimal mental model when dealing with interfaces - there's only one type of object you need to worry about: the ViewModel. It is where all the view logic happens, and manipulating the ViewModel will automatically keep the View and the Model in sync. Actuall DOM manipulations and output formatting are abstracted away into **[Directives]** and **[Filters]**.

VueJS is:

- **Lightweight**
  
    The standalone version of VueJS weighs around 10.5kb when minified and gzipped. It has no external dependencies at all. It is not designed to be an all-encompassing framework. You can mix and match it with anything you like, although it's also fairly trivial to implement ad-hoc validation and routing logic with only VueJS.

- **Simple**

    VueJS focuses on the interface only and has a minimal, declarative API. Creating a ViewModel is as simple as instantiating a new object with some passed-in options. It uses plain JS objects as the Model so no `get()` or `set()` verbosity. It provides automatic dependency tracking for computed properties and expressions. All of these features make it highly expressive: the included TodoMVC example is implemented with ~110 lines of code.

- **Fast**

    VueJS uses DOM-based templating and caches string templates as DOM fragments. Data bindings are bound to specific nodes for precise and efficient DOM manipulation with granularity down to a TextNode. VueJS also batches View updates to be executed asynchronously to avoid unnecesary updates. In the TodoMVC benchmark VueJS is [40% ~ 75% faster][benchmark] than the second fastest implementation (Backbone.js) across browsers.

- **Composable**

    VueJS ViewModels can be extended and nested, and each can contain its private directives, filters and child components. A re-usable component can be defined simply as a ViewModel option object, allowing them to be modularized, distributed and composed easily.
    
- **Module Friendly**

    VueJS is built with [Component], but it can also be used with [Browserify], with module loaders such as [RequireJS], or just as a standalone library.
    
Sounds good? [Let's get started](Getting-Started).

[benchmark]: Performance
[Component]: https://github.com/component/component
[Browserify]: http://browserify.org
[RequireJS]: http://requirejs.org
[ViewModel]: Concepts-Overview#viewmodel
[View]: Concepts-Overview#view
[Model]: Concepts-Overview#model
[Directives]: Concepts-Overview#directive
[Filters]: Concepts-Overview#filter