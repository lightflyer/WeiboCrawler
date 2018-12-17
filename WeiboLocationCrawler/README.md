# 基于位置信息页的微博爬虫

爬取微博位置信息页的微博数据，并写进sqlite数据库。

关于**微博位置信息页**打个比方，就是类似这个https://weibo.com/p/100101B2094757D069A7FE449F

![1543409340810](https://github.com/RealIvyWong/BlogBackup/raw/master/assets/1543409340810.png)

顺便一说，这个页面是不用微博登录就可以访问的。所以方便很多啊（不用模拟登录）。



包含四个文件。

## pid.csv

是放置地点的名称和微博页面对应的位置id。比如说上面的珞珈山，就是网页URL最后的那一串数字**100101B2094757D069A7FE449F**。

## buildip.py

是在网上看到别人写的……具体忘了哪的，如果本尊看到！sorry！请联系我注明！

我稍微修改了下。这个文件是一个实现爬取代理网站上的代理IP来构建代理池的模块。

## crawler.py

爬虫本体。

## start.py

控制爬取多个地点的一个启动文件。



所以要用这个爬虫，直接修改**pid.csv**里的位置ID后，修改下代码里的邮箱账号密码，然后运行**start.py**就可以用了！