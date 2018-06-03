# 电商评论抓取与观点挖掘系统
___
By Yu Yunfeng


## 介绍
___
本系统实现了京东、亚马逊两大电商平台上利用产品关键字对产品评论爬取，并且利用JST模型进行观点挖掘

## 使用
___
爬虫系统
```
/Spider/start.py是爬虫系统主程序，运行开始进行爬虫工作
setting.py对数据库进行设置
/Spider/Amazon_spider.py需要下载Chrome浏览器的驱动，可对商品数量、评论数量进行设置
```

分词系统
```
/NLP/parser.py利用jieba库分词，其中使用的用词字典、停用词词表均在/Date中
```


观点挖掘系统
```
/ReviewMing/JST/jst_pre.py是观点挖掘的主文件
/ReviewMing/JST/_jst.pyc是利用cython编写的吉布斯采样，MAC OS、Linux、windows下均可使用
/Data/comments.txt是从数据库中提取的，第一个数字代表打分，第二部分代表评论内容
```

