# R & Git Learning Community

欢迎来到R & Git Learning Community，具体说明请看这里：http://bzrlc.github.io/about/ .


## 使用方法

需要配好ruby环境，下载jekyll
(关于这个，小赵有时间会写专门写一篇文章介绍的)

需要下载的包：
+ `install.packages("servr")`
+ `devtools::install_github("brendan-R/brocks")`

建议参考这里 <https://github.com/brendan-r/jekyll-rstudio-demo/blob/master/README.md>

一切就绪后      
你只需要clone到本地，然后在`_source`文件夹下放入对应的 `.Rmd`和数据包(.csv ...),然后 `servr::jekyll`;

最后使用git'三板斧'：

```
git add .
git commit -m "随便说的什么啊"
git push origin master
```
你就可以去网站看生成的效果了 :)
