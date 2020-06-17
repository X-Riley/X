1.BFC是什么
2.BFC的布局规则
3.BFC有什么用
4.如何实现BFC
##BFC是什么

BFC指的是每个盒子都有独立的布局环境，其中的元素布局不受外界影响，也不影响外界
##BFC的布局规则

-内部的Box会在垂直方向，一个接一个地放置。
-Box垂直方向的距离由margin决定。属于同一个BFC的两个相邻Box的margin会发生重叠。
-每个盒子（块盒与行盒）的margin box的左边，与包含块border box的左边相接触(对于从左往右的格式化，否则相反)。即使存在浮动也是如此。
-BFC的区域不会与float box重叠。
-计算BFC的高度时，浮动元素也参与计算。
##BFC有什么用

-利用BFC避免margin重叠。
-自适应两栏布局
-清除浮动

##如何实现BFC

1.float的值不是none。
2.position的值不是static或者relative。
3.display的值是inline-block、table-cell、flex、table-caption或者inline-flex
4.overflow的值不是visible