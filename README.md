*This repository is a mirror of the [component](http://component.io) module [spini/backbone-router](http://github.com/spini/backbone-router). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/spini-backbone-router`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# backbone-router

  Backbone.Router [component](https://github.com/component/component/wiki/Components)

## Installation

    $ component install spini/backbone-router

## History stuff

It provides `Router.history` instead of `Backbone.history`

## Example

```js

var Router = require('spini-backbone-router');

var Workspace = Router.extend({

  routes: {
    "help":                 "help",    // #help
    "search/:query":        "search",  // #search/kiwis
    "search/:query/p:page": "search"   // #search/kiwis/p7
  },

  help: function() {
    ...
  },

  search: function(query, page) {
    ...
  }

});

```

# instantiate your Router

```

var myrouter = new Router(options);

```


# and then start history

```

Router.history.start({pushState: true});

// or

Router.history.start();

```


## API

See documentation for [Backbone.Router](http://backbonejs.org/#Router)

## License

[MIT](https://github.com/spini/backbone-router/blob/master/LICENSE)
