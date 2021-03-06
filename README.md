# Cancelable [![Build Status](https://drone.io/github.com/FGRibreau/cancelable/status.png)](https://drone.io/github.com/FGRibreau/cancelable/latest)

Cancelable functions for JavaScript.

## Getting Started
Install the module with: `npm install cancelable`

## Examples

```javascript
var Cancelable = require('cancelable');
var fn = Cancelable(function(){console.log('plop');});
fn(); // print "plop"
fn.cancel();
fn(); // do nothing
```

Cancelable is compatible with [Underscore](http://underscorejs.org/) and [Lodash](http://lodash.com/) as a mixin.

```javascript
var _ = require('underscore');
_.mixin(require('cancelable').exports());
var fn = _.cancelable(function(){console.log('plop');});
fn(); // print "plop"
fn.cancel();
fn(); // do nothing
```
## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [grunt](https://github.com/cowboy/grunt).

## Release History
v0.1.0 3/17/2013 Initial release.

## License
Copyright (c) 2013 Francois-Guillaume Ribreau
Licensed under the MIT license.
