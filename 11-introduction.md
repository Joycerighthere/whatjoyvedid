# zhan.com

## 输入

入口页面：[http://top.zhan.com/ielts/](http://top.zhan.com/ielts/)

四个板块：阅读/写作/听力/口语

听力：[http://top.zhan.com/ielts/listen/cambridge.html](http://top.zhan.com/ielts/listen/cambridge.html)

阅读：[http://top.zhan.com/ielts/read/cambridge.html](http://top.zhan.com/ielts/read/cambridge.html)

口语：[http://top.zhan.com/ielts/speak/cambridge.html](http://top.zhan.com/ielts/speak/cambridge.html)

写作：[http://top.zhan.com/ielts/write/cambridge.html](http://top.zhan.com/ielts/write/cambridge.html)

看每个板块的回顾部分



## 输出

每个抓取的页面需要存储页面内容到文件目录，.html ，并在数据库中记录 url、文件路径

![](http://ossp.pengjunjie.com/mweb/15573122965100.jpg)

说明：

每个page代表一个抓取页，需要把每个抓取页存储

url : 记录抓取页面的url链接 filename: 存储的文件名，记录在数据库中 path:存储的位置，记录在数据库中

#### ielts考试item模块对应

items：

一篇Reading文章对应一个item：[http://top.zhan.com/ielts/read/review-658-1-1.html](http://top.zhan.com/ielts/read/review-658-1-1.html)

一篇Listening文章对应一个item \(mp3可能是包含三个的\)：[http://top.zhan.com/ielts/listen/review-661-1-01.html](http://top.zhan.com/ielts/listen/review-661-1-01.html)

一个Writing对应一个\(分小作文和大作文\)，一个part一个item：[http://top.zhan.com/ielts/write/review-0-665-1.html](http://top.zhan.com/ielts/write/review-0-665-1.html)

一个口语题对应一个item：[http://top.zhan.com/ielts/speak/review-0-667-1.html](http://top.zhan.com/ielts/speak/review-0-667-1.html)



#### item-details

##### collection\_name:

对应每一个板块（阅读/写作/。。）

xpath：//\*\[@id="hm\_header"\]/div\[2\]/ul/li\[2\]/a

![](file:///Users/apple/Library/Application%20Support/typora-user-images/image-20190512115313379.png?lastModify=1558253740)



##### practice\_name

各板块xpath：//\*\[@id="crumbs"\]/a\[4\]/text\(\)

##### ![](file:///Users/apple/Library/Application%20Support/typora-user-images/image-20190512122651906.png?lastModify=1558253740)



##### title:

文章的标题

xpath：//\[@class="article\_title"\]/text\(\)

![](file:///Users/apple/Library/Application%20Support/typora-user-images/image-20190512120613898.png?lastModify=1558253740)



##### article\_content:

阅读/听力的文章内容

阅读xpath：//div\[@class="drag\_area\_left\_noimg canDoDrag pull-left"\]

听力xpath：//div\[@class="nano-slider"\]



![](file:///Users/apple/Library/Application%20Support/typora-user-images/image-20190512115435396.png?lastModify=1558253740)



##### article\_html:

这里记录整体的HTML\(阅读/听力\)

xpath同上

##### question\_content:

各个板块的题目

阅读xpath：'//div\[@class="question"\]'

听力xpath：'//div\[@class="drag\_content fillBlank\_content canDoDrag drag\_fillblank"\]'

写作xpath：‘//div\[@class="nano-content\_in ielts\_article"\]‘

口语xpath：'//p\[@class="MsoListParagraph"\]'

![](file:///Users/apple/Library/Application%20Support/typora-user-images/image-20190512115702853.png?lastModify=1558253740)

##### question\_html:同上

##### answer：

阅读xpath：'//label\[@class="radio\_error"\]'

听力xpath：

![](file:///Users/apple/Library/Application%20Support/typora-user-images/image-20190512120121022.png?lastModify=1558253740)

![](file:///Users/apple/Library/Application%20Support/typora-user-images/image-20190512120144520.png?lastModify=1558253740)



区别在于：class不同

##### answer\_html: 答案的HTML格式

##### order: 阅读、听力文章的顺序。单篇的存储方式可以使用。



##### sub\_type：只适用于writing，区分task1或task2

![](file:///Users/apple/Library/Application%20Support/typora-user-images/image-20190512122029393.png?lastModify=1558253740)



xpath：

#### listening：

##### practice\_name:

//\*\[@id="crumbs"\]/a\[4\]











### 



