常见的水平和垂直居中只是简单提下，后面的 CSS3 方法我会写 demo 测试

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

