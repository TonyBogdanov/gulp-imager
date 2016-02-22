# Gulp-Imager

[![Buy Me a Coffee](http://static.tonybogdanov.com/github/coffee.svg)](http://ko-fi.co/1236KUKJNC96B)

Gulp wrapper for [TonyBogdanov/imager](https://github.com/TonyBogdanov/imager)'s `generate` method.

## Installing

```shell
$ npm install --save-dev gulp-imager
```

## Usage

```js
var imager = require('gulp-imager');

gulp.task('images', function() {
    return imager();
});

// or

gulp.task('images', function() {
    return imager({
        cwd: '/path/to/current/working/directory',
        json: '/path/to/imager.json',
        cmd: '-vv'
    });
});
```

The function accepts a single optional argument of type `object` with the following structure:

Key         | Description
---         | ---
`cwd`       | A valid path to `cd` to and use as the current working directory.
`json`      | Path to a valid `imager.json` file, defaults to `imager.json` in the `cwd`.
`cmd`       | Additional command line arguments to be relayed to imager.

## CLI

If you need a console-only solution, just use the [TonyBogdanov/imager](https://github.com/TonyBogdanov/imager)
package.