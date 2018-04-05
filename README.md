使用fullPage+css3：

   fullPage.js 是一个基于 jQuery 的插件，它能够很方便、很轻松的制作出全屏网站。
   主要功能有：

	支持鼠标滚动

	支持前进后退和键盘控制

	多个回调函数

	支持手机、平板触摸事件

	支持 CSS3 动画

	支持窗口缩放

	窗口缩放时自动调整

	可设置滚动宽度、背景颜色、滚动速度、循环选项、回调、文本对齐方式等等
   
    更好的用户体验
	

使用方法：

1、引入文件
<link rel="stylesheet" href="css/jquery.fullPage.css">
<script src="js/jquery.min.js"></script>
 
<!-- jquery.easings.min.js 是必须的，用于 easing 参数，也可以使用完整的 jQuery UI 代替 -->
<script src="js/jquery.easings.min.js"></script>
 
<!-- 如果 scrollOverflow 设置为 true，则需要引入 jquery.slimscroll.min.js，一般情况下不需要 -->
<script src="js/jquery.slimscroll.min.js"></script>
 
<script src="js/jquery.fullPage.js"></script>

2、HTML
<div id="fullpage">
    <div class="section">第一屏</div>
    <div class="section">第二屏</div>
    <div class="section">
        <div class="slide">第三屏的第一屏</div>
        <div class="slide">第三屏的第二屏</div>
        <div class="slide">第三屏的第三屏</div>
        <div class="slide">第三屏的第四屏</div>
    </div>
    <div class="section">第四屏</div>
</div>

3、JavaScript
$(function(){
    $('#fullpage').fullpage();
});

回调函数
afterLoad	滚动到某一屏后的回调函数，接收 anchorLink 和 index 两个参数，anchorLink 是锚链接的名称，index 是序号，从1开始计算
onLeave		滚动前的回调函数，接收 index、nextIndex 和 direction 3个参数：
index 		是离开的“页面”的序号，从1开始计算；

nextIndex 	是滚动到的“页面”的序号，从1开始计算；

direction 	判断往上滚动还是往下滚动，值是 up 或 down。

afterRender	页面结构生成后的回调函数，或者说页面初始化完成后的回调函数
afterSlideLoad	滚动到某一水平滑块后的回调函数，与 afterLoad 类似，接收 anchorLink、index、slideIndex、direction 4个参数
onSlideLeave	某一水平滑块滚动前的回调函数，与 onLeave 类似，接收 anchorLink、index、slideIndex、direction 4个参数