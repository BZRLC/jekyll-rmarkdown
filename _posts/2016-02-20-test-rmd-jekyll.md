---
layout: post
title: "Serve Rmds with Jekyll(citations)"
author: "Vasilios Zachariadis"
date: "20 February 2016"
---



## R Markdown

Thiss is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that includes both content as well as the output of any embedded R code chunks within the document. You can embed an R code chunk like this:


{% highlight r %}
summary(cars)
{% endhighlight %}



{% highlight text %}
##      speed           dist       
##  Min.   : 4.0   Min.   :  2.00  
##  1st Qu.:12.0   1st Qu.: 26.00  
##  Median :15.0   Median : 36.00  
##  Mean   :15.4   Mean   : 42.98  
##  3rd Qu.:19.0   3rd Qu.: 56.00  
##  Max.   :25.0   Max.   :120.00
{% endhighlight %}

## Including Plots

You can also embed plots, for example:

![plot of chunk pressure](/figure/source/2016-02-20-test-rmd-jekyll/pressure-1.png)

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.


{% highlight r %}
library(magrittr)
library(highcharter)
highchart() %>% 
  hc_title(text = "Scatter chart with size and color") %>% 
  hc_add_serie_scatter(mtcars$wt, mtcars$mpg,
                       mtcars$drat, mtcars$hp)
{% endhighlight %}

<!--html_preserve--><div id="htmlwidget-5141" style="width:100%;height:500px;" class="highchart html-widget"></div>
<script type="application/json" data-for="htmlwidget-5141">{"x":{"hc_opts":{"title":{"text":"Scatter chart with size and color"},"credits":{"enabled":false},"exporting":{"enabled":false},"plotOptions":{"series":{"turboThreshold":0}},"series":[{"data":[{"x":2.62,"y":21,"z":3.9,"valuecolor":110,"color":"#26828EFF"},{"x":2.875,"y":21,"z":3.9,"valuecolor":110,"color":"#26828EFF"},{"x":2.32,"y":22.8,"z":3.85,"valuecolor":93,"color":"#3E4989FF"},{"x":3.215,"y":21.4,"z":3.08,"valuecolor":110,"color":"#26828EFF"},{"x":3.44,"y":18.7,"z":3.15,"valuecolor":175,"color":"#3EBC74FF"},{"x":3.46,"y":18.1,"z":2.76,"valuecolor":105,"color":"#33628DFF"},{"x":3.57,"y":14.3,"z":3.21,"valuecolor":245,"color":"#D6E21AFF"},{"x":3.19,"y":24.4,"z":3.69,"valuecolor":62,"color":"#481769FF"},{"x":3.15,"y":22.8,"z":3.92,"valuecolor":95,"color":"#3B528BFF"},{"x":3.44,"y":19.2,"z":3.92,"valuecolor":123,"color":"#1F978BFF"},{"x":3.44,"y":17.8,"z":3.92,"valuecolor":123,"color":"#1F978BFF"},{"x":4.07,"y":16.4,"z":3.07,"valuecolor":180,"color":"#6ECE58FF"},{"x":3.73,"y":17.3,"z":3.07,"valuecolor":180,"color":"#6ECE58FF"},{"x":3.78,"y":15.2,"z":3.07,"valuecolor":180,"color":"#6ECE58FF"},{"x":5.25,"y":10.4,"z":2.93,"valuecolor":205,"color":"#81D34DFF"},{"x":5.424,"y":10.4,"z":3,"valuecolor":215,"color":"#95D840FF"},{"x":5.345,"y":14.7,"z":3.23,"valuecolor":230,"color":"#AADC32FF"},{"x":2.2,"y":32.4,"z":4.08,"valuecolor":66,"color":"#453681FF"},{"x":1.615,"y":30.4,"z":4.93,"valuecolor":52,"color":"#470C5FFF"},{"x":1.835,"y":33.9,"z":4.22,"valuecolor":65,"color":"#482374FF"},{"x":2.465,"y":21.5,"z":3.7,"valuecolor":97,"color":"#375A8CFF"},{"x":3.52,"y":15.5,"z":2.76,"valuecolor":150,"color":"#21A685FF"},{"x":3.435,"y":15.2,"z":3.15,"valuecolor":150,"color":"#21A685FF"},{"x":3.84,"y":13.3,"z":3.73,"valuecolor":245,"color":"#D6E21AFF"},{"x":3.845,"y":19.2,"z":3.08,"valuecolor":175,"color":"#3EBC74FF"},{"x":1.935,"y":27.3,"z":4.08,"valuecolor":66,"color":"#453681FF"},{"x":2.14,"y":26,"z":4.43,"valuecolor":91,"color":"#424086FF"},{"x":1.513,"y":30.4,"z":3.77,"valuecolor":113,"color":"#23888EFF"},{"x":3.17,"y":15.8,"z":4.22,"valuecolor":264,"color":"#EAE51AFF"},{"x":2.77,"y":19.7,"z":3.62,"valuecolor":175,"color":"#3EBC74FF"},{"x":3.57,"y":15,"z":3.54,"valuecolor":335,"color":"#FDE725FF"},{"x":2.78,"y":21.4,"z":4.11,"valuecolor":109,"color":"#2F6B8EFF"}],"type":"bubble","showInLegend":false}]},"theme":null,"conf_opts":{"global":{"Date":null,"VMLRadialGradientURL":"http =//code.highcharts.com/list(version)/gfx/vml-radial-gradient.png","canvasToolsURL":"http =//code.highcharts.com/list(version)/modules/canvas-tools.js","getTimezoneOffset":null,"timezoneOffset":0,"useUTC":true},"lang":{"contextButtonTitle":"Chart context menu","decimalPoint":".","downloadJPEG":"Download JPEG image","downloadPDF":"Download PDF document","downloadPNG":"Download PNG image","downloadSVG":"Download SVG vector image","drillUpText":"Back to {series.name}","invalidDate":null,"loading":"Loading...","months":["January","February","March","April","May","June","July","August","September","October","November","December"],"noData":"No data to display","numericSymbols":["k","M","G","T","P","E"],"printChart":"Print chart","resetZoom":"Reset zoom","resetZoomTitle":"Reset zoom level 1:1","shortMonths":["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"],"thousandsSep":" ","weekdays":["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"]}},"type":"chart","fonts":[],"debug":false},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->


{% highlight r %}
library(DT)
datatable(iris, options = list(pageLength = 5))
{% endhighlight %}

<!--html_preserve--><div id="htmlwidget-2357" style="width:100%;height:auto;" class="datatables html-widget"></div>
<script type="application/json" data-for="htmlwidget-2357">{"x":{"data":[["1","2","3","4","5","6","7","8","9","10","11","12","13","14","15","16","17","18","19","20","21","22","23","24","25","26","27","28","29","30","31","32","33","34","35","36","37","38","39","40","41","42","43","44","45","46","47","48","49","50","51","52","53","54","55","56","57","58","59","60","61","62","63","64","65","66","67","68","69","70","71","72","73","74","75","76","77","78","79","80","81","82","83","84","85","86","87","88","89","90","91","92","93","94","95","96","97","98","99","100","101","102","103","104","105","106","107","108","109","110","111","112","113","114","115","116","117","118","119","120","121","122","123","124","125","126","127","128","129","130","131","132","133","134","135","136","137","138","139","140","141","142","143","144","145","146","147","148","149","150"],[5.1,4.9,4.7,4.6,5,5.4,4.6,5,4.4,4.9,5.4,4.8,4.8,4.3,5.8,5.7,5.4,5.1,5.7,5.1,5.4,5.1,4.6,5.1,4.8,5,5,5.2,5.2,4.7,4.8,5.4,5.2,5.5,4.9,5,5.5,4.9,4.4,5.1,5,4.5,4.4,5,5.1,4.8,5.1,4.6,5.3,5,7,6.4,6.9,5.5,6.5,5.7,6.3,4.9,6.6,5.2,5,5.9,6,6.1,5.6,6.7,5.6,5.8,6.2,5.6,5.9,6.1,6.3,6.1,6.4,6.6,6.8,6.7,6,5.7,5.5,5.5,5.8,6,5.4,6,6.7,6.3,5.6,5.5,5.5,6.1,5.8,5,5.6,5.7,5.7,6.2,5.1,5.7,6.3,5.8,7.1,6.3,6.5,7.6,4.9,7.3,6.7,7.2,6.5,6.4,6.8,5.7,5.8,6.4,6.5,7.7,7.7,6,6.9,5.6,7.7,6.3,6.7,7.2,6.2,6.1,6.4,7.2,7.4,7.9,6.4,6.3,6.1,7.7,6.3,6.4,6,6.9,6.7,6.9,5.8,6.8,6.7,6.7,6.3,6.5,6.2,5.9],[3.5,3,3.2,3.1,3.6,3.9,3.4,3.4,2.9,3.1,3.7,3.4,3,3,4,4.4,3.9,3.5,3.8,3.8,3.4,3.7,3.6,3.3,3.4,3,3.4,3.5,3.4,3.2,3.1,3.4,4.1,4.2,3.1,3.2,3.5,3.6,3,3.4,3.5,2.3,3.2,3.5,3.8,3,3.8,3.2,3.7,3.3,3.2,3.2,3.1,2.3,2.8,2.8,3.3,2.4,2.9,2.7,2,3,2.2,2.9,2.9,3.1,3,2.7,2.2,2.5,3.2,2.8,2.5,2.8,2.9,3,2.8,3,2.9,2.6,2.4,2.4,2.7,2.7,3,3.4,3.1,2.3,3,2.5,2.6,3,2.6,2.3,2.7,3,2.9,2.9,2.5,2.8,3.3,2.7,3,2.9,3,3,2.5,2.9,2.5,3.6,3.2,2.7,3,2.5,2.8,3.2,3,3.8,2.6,2.2,3.2,2.8,2.8,2.7,3.3,3.2,2.8,3,2.8,3,2.8,3.8,2.8,2.8,2.6,3,3.4,3.1,3,3.1,3.1,3.1,2.7,3.2,3.3,3,2.5,3,3.4,3],[1.4,1.4,1.3,1.5,1.4,1.7,1.4,1.5,1.4,1.5,1.5,1.6,1.4,1.1,1.2,1.5,1.3,1.4,1.7,1.5,1.7,1.5,1,1.7,1.9,1.6,1.6,1.5,1.4,1.6,1.6,1.5,1.5,1.4,1.5,1.2,1.3,1.4,1.3,1.5,1.3,1.3,1.3,1.6,1.9,1.4,1.6,1.4,1.5,1.4,4.7,4.5,4.9,4,4.6,4.5,4.7,3.3,4.6,3.9,3.5,4.2,4,4.7,3.6,4.4,4.5,4.1,4.5,3.9,4.8,4,4.9,4.7,4.3,4.4,4.8,5,4.5,3.5,3.8,3.7,3.9,5.1,4.5,4.5,4.7,4.4,4.1,4,4.4,4.6,4,3.3,4.2,4.2,4.2,4.3,3,4.1,6,5.1,5.9,5.6,5.8,6.6,4.5,6.3,5.8,6.1,5.1,5.3,5.5,5,5.1,5.3,5.5,6.7,6.9,5,5.7,4.9,6.7,4.9,5.7,6,4.8,4.9,5.6,5.8,6.1,6.4,5.6,5.1,5.6,6.1,5.6,5.5,4.8,5.4,5.6,5.1,5.1,5.9,5.7,5.2,5,5.2,5.4,5.1],[0.2,0.2,0.2,0.2,0.2,0.4,0.3,0.2,0.2,0.1,0.2,0.2,0.1,0.1,0.2,0.4,0.4,0.3,0.3,0.3,0.2,0.4,0.2,0.5,0.2,0.2,0.4,0.2,0.2,0.2,0.2,0.4,0.1,0.2,0.2,0.2,0.2,0.1,0.2,0.2,0.3,0.3,0.2,0.6,0.4,0.3,0.2,0.2,0.2,0.2,1.4,1.5,1.5,1.3,1.5,1.3,1.6,1,1.3,1.4,1,1.5,1,1.4,1.3,1.4,1.5,1,1.5,1.1,1.8,1.3,1.5,1.2,1.3,1.4,1.4,1.7,1.5,1,1.1,1,1.2,1.6,1.5,1.6,1.5,1.3,1.3,1.3,1.2,1.4,1.2,1,1.3,1.2,1.3,1.3,1.1,1.3,2.5,1.9,2.1,1.8,2.2,2.1,1.7,1.8,1.8,2.5,2,1.9,2.1,2,2.4,2.3,1.8,2.2,2.3,1.5,2.3,2,2,1.8,2.1,1.8,1.8,1.8,2.1,1.6,1.9,2,2.2,1.5,1.4,2.3,2.4,1.8,1.8,2.1,2.4,2.3,1.9,2.3,2.5,2.3,1.9,2,2.3,1.8],["setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","setosa","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","versicolor","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica","virginica"]],"container":"<table class=\"display\">\n  <thead>\n    <tr>\n      <th> \u003c/th>\n      <th>Sepal.Length\u003c/th>\n      <th>Sepal.Width\u003c/th>\n      <th>Petal.Length\u003c/th>\n      <th>Petal.Width\u003c/th>\n      <th>Species\u003c/th>\n    \u003c/tr>\n  \u003c/thead>\n\u003c/table>","options":{"pageLength":5,"columnDefs":[{"className":"dt-right","targets":[1,2,3,4]},{"orderable":false,"targets":0}],"order":[],"autoWidth":false,"orderClasses":false,"lengthMenu":[5,10,25,50,100]},"callback":null,"filter":"none"},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->

## End
