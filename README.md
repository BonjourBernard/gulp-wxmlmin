# gulp-wxmlmin
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
