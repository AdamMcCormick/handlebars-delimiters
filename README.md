# handlebars-delimiters [![NPM version](https://badge.fury.io/js/handlebars-delimiters.svg)](http://badge.fury.io/js/handlebars-delimiters)


> Custom delimiters, for Handlebars templates.

## Install
#### Install with [npm](npmjs.org)

```bash
npm i handlebars-delimiters --save
```

## Run tests

```bash
npm test
```

## Usage

```js
var Handlebars = require('handlebars');
var useDelims = require('handlebars-delimiters');

var a = Handlebars.compile('{{ name }}<%= name %>')({name: 'Jon'});
console.log(a);
//=> 'Jon<%= name %>'


// Pass your instance of Handlebars and define custom delimiters
useDelims(Handlebars, ['<%=', '%>']);
var b = Handlebars.compile('{{ name }}<%= name %>')({name: 'Jon'});
console.log(b);
//=> '{{ name }}Jon'
```

## Author

**Jon Schlinkert**
 
+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert) 

## License
Copyright (c) 2014 Jon Schlinkert, contributors.  
Released under the MIT license

***

_This file was generated by [verb-cli](https://github.com/assemble/verb-cli) on September 14, 2014._