# gulp-wxmlmin
其实就是gulp-htmlmin编译的话，因为小程序input写法问题 以及自定义属性会转成小写等导致页面报错，就把这些问题处理了下

wxml  gulp 压缩
## 安装
```
npm install gulp-wxml-min --save-dev
```
## 使用
```
var wxmlmin = require('gulp-wxml-min')

gulp.src(path.src)
.pipe(wxmlmin({
  collapseWhitespace: true,
  removeComments: true,
  keepClosingSlash: true
}))
.pipe(gulp.dest(path.dest))
```
