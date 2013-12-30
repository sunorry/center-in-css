本来说顺便把 display: flex; 带进去，但是看了标准再加上自己从来没有用过，感觉自己差太远了，所以现在把里介绍这里的东西都删掉，以后再加个库吧。

# 水平居中 #

(1)<b>text-align: center;</b>

只能用在块级元素上，此块级元素的子元素(必须是 inline content)就可以居中了。

(2)<b>margin: auto;</b>

用在块级元素上，而且必须指定宽度。

(3)还有一种是绝对定位，left: 50%; margin-left: -(width)px; 此方法也可垂直居中。

# 垂直居中 #

(1)<b>height = line-height</b>

文字居中,关于 line-heght 有几点说明下，

①在块级元素里， line-height 用来指定里面行框的最小高度；

②在非置换行内元素里， line-height 用来计算行框的高度；

③在置换行内元素使用 inline-height 是没用的。(现在所有的浏览器在这点都实现错了)

(2)<b>display: table-cell; vertical-align: middle;</b>

# CSS3 方法 #

(1) display: flex;

-webkit-align-items: center; align-items: center; 再指定高度，这样就可以让里面的指定高度的子元素竖直居中了。