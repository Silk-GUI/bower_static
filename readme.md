Bower Static
------------

Adds routing for bower folder.

Example

```js

var express = require('express');
var app = express();

// Bower static tries to find the app root
// but in some situations it can be wrong.
// This folder should be the parent folder for
// the bower_components folder.
bowerStatic.changeAppRoot(__dirname);
app.use('/bc', bowerStatic);

// add other routes here

app.listen(3000);
console.log('listening at 3000');

```

If you installed jquery with bower, this
will load jquery:
 ```html
 <script src="/bc/jquery"></script>
```