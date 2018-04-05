# First heading
## Second heading
### Third heading
[KamilRogala.IT](https://kamilrogala.it)- check my blog (in polish language at this commit time)

Some section
--------------------------------------

- list
- list
- list

1. list
2. list
3. list

- [ ] List
- [ ] List
- [x] List

Some other section
--------------------------------------
**Some bolded stuff**
**Some bolded stuff**
**Some bolded stuff**

_Some italic stuff_
_Some italic stuff_
_Some italic stuff_

Some another section
--------------------------------------

> My very stupid quote

> Quote of my dog

> random Stuff

Lets code!

```js
const gulp = require('gulp');
const sass = require('gulp-sass');
const sourcemaps = require('gulp-sourcemaps');
const autoprefixer = require('gulp-autoprefixer');
const cleanCSS = require('gulp-clean-css');
const uglify = require('gulp-uglify');
const concat = require('gulp-concat');

gulp.task('default', ['sass'], () => {
  console.log('poszlo');
});

gulp.task('uglify', () => {
  return gulp.src('./src/js/**/*.js')
  .pipe(concat('script.js'))
  .pipe(uglify())
  .pipe(gulp.dest('./dist/js'));
});
gulp.task('concaar', () => {});
gulp.task('prefix', () => {});

gulp.task('css', () => {
  gulp.src('./src/css/**/*.css')
    .pipe(concat('style.css'))
    .pipe(cleanCSS())
    .pipe(gulp.dest('./dist/css'))
});

gulp.task('sass', () => {
  console.log('odpalam sass')
  return gulp.src('./src/scss/**/*.scss')
    .pipe(sourcemaps.init())
    .pipe(sass().on('error', sass.logError))
    .pipe(autoprefixer({
      browsers: ['last 70 versions']
    }))
    .pipe(sourcemaps.write())
    .pipe(gulp.dest('./src/css'));
});

gulp.watch('./src/scss/**/*.scss', ['sass']);
gulp.watch('./src/css/**/*.css', ['css']);
gulp.watch('./src/js/**/*.js', ['uglify']);
```

Yet one more section
--------------------------------------

Just trying more stuff

@kamilrogala

#3588 