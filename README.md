# Nunjucks filter `filesizeformat`

[![Build Status](https://travis-ci.org/jbmoelker/nunjucks-filter-filesizeformat.svg?branch=master)](https://travis-ci.org/jbmoelker/nunjucks-filter-filesizeformat)

[Nunjucks](https://mozilla.github.io/nunjucks/) [filter](https://mozilla.github.io/nunjucks/templating.html#filters) to format a value like a ‘human-readable’ file size (i.e. 13 kB, 4.1 MB, 102 Bytes, etc).

This filter is based on and compatible with the [Jinja2 `filesizeformat` filter](http://jinja.pocoo.org/docs/dev/templates/#filesizeformat).


## Install

```bash
$ npm install --save nunjucks-filter-filesizeformat
```

## Usage

Install as [custom filter](https://mozilla.github.io/nunjucks/api#custom-filters):

```javascript
var nunjucks = require('nunjucks');
var filesizeformat = require('nunjucks-filter-filesizeformat');

var env = new nunjucks.Environment();
env.addFilter('filesizeformat', filesizeformat);
```

Use in template:

```jinja
{{ 1230456|filesizeformat }}
```

Outputs `1.2 MB`


## API

### `filesizeformat(input, [binary])`

### input

Type: `number`

Value to format as ‘human-readable’ file size (i.e. 13 kB, 4.1 MB, 102 Bytes, etc).

### binary

Type: `boolean`<br>
Default: `false`

Per default decimal units are used (Mega, Giga, etc.).
If binary is true, binary units are used (Mebi, Gibi).


## Support

Same support as Nunjucks:
* Node >= v0.10
* all modern browsers
* IE8 requires [es5-shim](https://github.com/es-shims/es5-shim)


## License

[MIT Licensed](LICENSE) © [Jasper Moelker](https://twitter.com/jbmoelker)
