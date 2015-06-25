<!-- 
.. title: aiohttp-抓取多看图书列表
.. slug: aiohttp-zhua-qu-duo-kan-tu-shu-lie-biao
.. date: 2014-09-03 16:22:38 UTC+08:00
.. tags: Python
.. link: 
.. description: 
.. type: text
-->

[多看](http://www.duokan.com/list/1-1)大赦三天(0901-0903), 看看热闹, 试用[aiohttp](https://github.com/KeepSafe/aiohttp)抓列表.支持多看, 支持正版.

<!-- TEASER_END-->

输出结果为: 图书名 id号

###时间统计

1. [全部图书 28089](http://pan.baidu.com/s/1ntDj2Jn)
    ```
    real    6m38.412s
    user    6m19.044s
    sys 0m2.171s
    ```
2. [计算机类图书 530](http://pan.baidu.com/s/1o6BL7zs)
    ```
    real    0m7.703s
    user    0m7.310s
    sys 0m0.080s
    ```

###Code

<script src="https://gist.github.com/muxuezi/2b8b51076291d483f93c.js"></script>

在如下链接中填如对应图书id即可打开图书:

```
http://www.duokan.com/reader/www/app.html?id=...
```

Reference from [Fast scraping in python with asyncio (Georges Dubus)](http://compiletoi.net/fast-scraping-in-python-with-asyncio.html)

