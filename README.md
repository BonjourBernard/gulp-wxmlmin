# gulp-wxmlmin
其实就是gulp-htmlmin编译的话，因为小程序input写法问题 以及自定义属性会转成小写等导致页面报错，就把这些问题处理了下 用法和gulp-htmlmin一致

wxml  gulp 压缩
## 安装
```
npm install gulp-wxml-min --save-dev
```
## 使用
```
var wxmlmin = require('gulp-wxml-min')

<!-- removeComments: true,//清除HTML注释
     collapseWhitespace: true,//压缩HTML
     collapseBooleanAttributes: true,//省略布尔属性的值 <input checked="true"/> ==> <input />
     removeEmptyAttributes: true,//删除所有空格作属性值 <input id="" /> ==> <input />
     keepClosingSlash: true, // 单标签上保留斜线
-->
gulp.src(path.src)
.pipe(wxmlmin({
  collapseWhitespace: true,
  removeComments: true,
  keepClosingSlash: true
}))
.pipe(gulp.dest(path.dest))
```
