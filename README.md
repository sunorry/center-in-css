本来说顺便把 display: flex; 带进去，但是看了标准再加上自己从来没有用过，感觉自己差太远了，所以现在把里介绍这里的东西都删掉，以后再加个库吧。

# 水平居中 #

(1)<b>text-align: center;</b>

只能用在块级元素上，此块级元素的子元素(必须是 inline content)就可以居中了。

(2)<b>margin: auto;</b>

用在块级元素上，而且必须指定宽度。

(3)还有一种是绝对定位，left: 50%; margin-left: -(width)px; 此方法也可垂直居中（如果有 padding 的话 (width + padding)/2 ）。

# 垂直居中 #

(1)<b>height = line-height</b>

文字居中,关于 line-heght 有几点说明下，

①在块级元素里， line-height 用来指定里面行框的最小高度；

②在非置换行内元素里， line-height 用来计算行框的高度；

③在置换行内元素使用 inline-height 是没用的。(现在所有的浏览器在这点都实现错了)

(2)<b>display: table-cell; vertical-align: middle;</b>

# 垂直水平居中 #

<b>margin: auto;  position: absolute; top: 0; left: 0; bottom: 0; right: 0;</b>

剩下的就是给元素加上宽高。

原理：

① <code>margin-left：auto;</code> 是计算方式是剩余空间，若 margin-right 为 0 ，那么它的计算值为 可视区宽减元素宽，所以 margin: 0 auto; 可以左右居中，<code>margin-top/bottom:auto</code> 会计算为 0 。

②top: 0; left: 0; bottom: 0; right: 0; 样式的块元素会让浏览器为它包裹一层新的盒子，因此这个元素会填满它相对父元素的内部空间，这个相对父元素可以是是body标签，或者是一个设置了position: relative; 样式的容器。(若父元素是 body ，那么你不设置宽高的话，它会充满整个 body 哦！)。

③在非置换元素上，Since the block is absolutely positioned and therefore out of the normal flow, the browser gives equal values to margin-top and margin-bottom centering the element in the bounds set earlier.
W3.org: If none of the three [top, bottom, height] are 'auto': If both 'margin-top' and 'margin-bottom' are 'auto', solve the equation under the extra constraint that the two margins get equal values. <b>AKA: center the block vertically</b>

# CSS3 方法 #

(1) <b>display: flex;</b>

-webkit-align-items: center; align-items: center; 再指定高度，这样就可以让里面的指定高度的子元素竖直居中了。

---

test
