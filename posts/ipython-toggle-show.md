<!-- 
.. title: 关于本站ipython动态显示
.. slug: ipython-toggle-show
.. date: 2014-09-12 14:57:53 UTC+08:00
.. tags: HTML/CSS, ipython
.. link: 
.. description: 
.. type: text
-->

**必须安装[ipython2.2](http://ipython.org/install.html#)**，ipython2.1不行，关键是toggle.tpl里面引用的basic.tpl在ipython2.2里面。

<!-- TEASER_END-->

按照[damian_blog](https://github.com/damianavila/damian_blog)添加自己的posts和stories就可以了，提交ipynb文件可以参照Start.ipynb。

config.py默认输出位置为OUTPUT_FOLDER = 'output'，nikola build之后就会自动生成output，我改为OUTPUT_FOLDER = 'muxuezi.github.io'了，方便github提交，我做了个update.sh：

```bash
nikola build
cd muxuezi.github.io
git add -A
git commit -m 'update'
git push origin master
```

Mathjax需要引入以下代码，否则ipynb文件不能显示：

```
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
```