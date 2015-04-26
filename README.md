autolinks for NW.js
=========

Automatically turn URL's into links

Installation
------------

To use locally

    download & extract in node_modules folder

Example
-------

``` js
var autolinks = require('autolinks');

var s = 'a nice text with a nice www.google.com link!';
console.log(s);
console.log('html => %s', autolinks(s));
console.log('markdown => %s', autolinks(s, 'markdown'));
```

yields

    a nice text with a nice www.google.com link!
    html => a nice text with a nice <a href="#" onclick="gui.Shell.openExternal('http://www.google.com');">www.google.com link!</a>
    markdown => my email is [dave@daveeddy.com](mailto:dave@daveeddy.com) and my homepage is [http://www.daveeddy.com](http://www.daveeddy.com)

Usage
-----

### `autolinks(s, [fmt])`

- `s`: the string to parse
- `fmt`: an optional format string (markdown, html, etc.) `html` is default

returns the parsed string

License
-------

MIT License
