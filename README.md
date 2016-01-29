gulp-closure-compiler-service
=============================
Gulp plugin to compile JavaScript with the Google
[Closure compiler service](https://developers.google.com/closure/compiler/docs/api-ref).
No Java dependency.

Installation
------------

    $ npm install gulp-closure-compiler-service

Usage
-----

```javascript
var closure = require('gulp-closure-compiler-service');

gulp.task('compile', function() {
  return gulp.src('src/*.js')
    .pipe(closure())
    .pipe(gulp.dest('dist'));
});
```

[Options](https://github.com/gavinhungry/closure-compiler-service/blob/master/README.md#default-options)
can be passed to the API:

```javascript
.pipe(closure({
  language: 'ECMASCRIPT5',
  compilation_level: 'WHITESPACE_ONLY'
}))
```

License
-------
This software is released under the terms of the **MIT license**. See `LICENSE`.
