# Custom command line tab completion for node.js applications.

## Using this module.

```
$npm install complete
```

### Require the module.

```javascript
var complete = require('complete');
```

### Install your program.

Your installment procedure should place your CLI program in a location made accessible by the `PATH` variable. If users install your program with the NPM `-g` option, your program will be in the path.

``` bash
/usr/local/bin/myprogram -> /usr/local/lib/node_modules/myprogram/bin/myprogram
```

## API

- After you put it in an accessible place, run it with the `--install` option. This will install a series of bash scripts in the `/usr/local/lib/node_scripts/` directory. Optionally, you can then add a script to your CLI program to ensure that it has been `installed`.

### Create a list of commands that you want to autocomplete with.

```javascript
complete.list = ['apple', 'orange', 'pear', 'lemon', 'mango'];
```

### Optionally you can define a callback that will get called when the match when the completion happens.

```javascript
complete.callback = function(lastSelection, userInput, reducedList) {
  
  //
  // do something if this is an `orange`. Note that anything that
  // you `process.stdout.write()` will be added to the auto complete 
  // list.
  //
};
```

### initialize the auto completion method.

```javascript
complete.init();
```

## Licence

(The MIT License)

Copyright (c) 2010 hij1nx <http://www.twitter.com/hij1nx>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the 'Software'), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

