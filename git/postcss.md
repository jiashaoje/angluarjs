
##  自动编译各种兼容css

let's  go

####  给予gulp

#### 代码如下


```
    var gulp =require("gulp");

 自动编译css

    gulp.task("postcss",function(){
          // 模块写在方法内就不在过多的内存
        var postcss =require("gulp-postcss"),       //css 解析平台
            autoprefixer=require("autoprefixer");   // 自动添加前缀

        return gulp.src("./*.css")     //在这里用的是正则匹配所有的.css
                .pipe(postcss([autoprefixer({browsers:['last 2 versions']})]))
                .pipe(gulp.dest('./dist/'))

    })


    gulp.task("default",["postcss"])  // 默认任务

```