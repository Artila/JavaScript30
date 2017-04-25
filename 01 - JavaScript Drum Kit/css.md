1、  <code>{pading:0;margin:0;}</code>

  采用这样的写法好处是写起来很简单，但是是通配符，需要把所有的标签都遍历一遍，当网站较大时，样式比较多，这样写就大大的加强了网站运行的负载，会使网站加载的时候需要很长一段时间，因此一般大型的网站都有分层次的一套初始化样式。

  这是出于性能考虑，并不是所有标签都会有padding和margin，因此对常见的具有默认padding和margin的元素初始化即可，并不需使用通配符*来初始化。

2、  <code>display: flex;</code>

这是 Flex 布局，具体可以看[阮一峰老师的教程]( http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html)。
目前，已经得到了所有浏览器的支持，这意味着，现在就能很安全地使用这项功能。

3、 ```min-height: 100vh;```

这是 CSS3 新增的单位。
>vw Viewport宽度， 1vw 等于viewport宽度的1%
vh Viewport高度， 1vh 等于viewport高的的1%

w和vh会随着viewport变化自动变化，再也不用js控制全屏了。
做一个占满高度的或者接近占满高度的部分时，你就可以用这行代码解决。另外，在 footer 置底的情况也用到它。

4、```align-items: center; /* 居中对齐 */```

>align-items 属性定义flex子项在flex容器的当前行的侧轴（纵轴）方向上的对齐方式。
注意: Internet Explorer 10 及更早版本浏览器不支持 align-items 属性。
注意: Safari 7.0 及更新版本通过 -webkit-align-items 属性支持该属性。

5、```justify-content: center; /* 居中对齐 */```

>justify-content 用于设置或检索弹性盒子元素在主轴（横轴）方向上的对齐方式。
注意: Internet Explorer 10 及更早版本浏览器不支持 justify-content 属性。
注意: Safari 6.1 及更新版本通过 -webkit-justify-content 属性支持该属性。

6、```rem```

rem（font size of the root element）是指相对于根元素的字体大小的单位。简单的说它就是一个相对单位。适合于手机网页。
网页中的根元素指的是html我们通过设置html的字体大小就可以控制rem的大小。
参考文章：[web app变革之rem](http://isux.tencent.com/web-app-rem.html)，[CSS3的REM设置字体大小](http://www.w3cplus.com/css3/define-font-size-with-css3-rem)

7、```text-transform: uppercase;```

>text-transform 属性控制文本的大小写。
capitalize	        文本中的每个单词以大写字母开头。
uppercase	定义仅有大写字母。
lowercase	定义无大写字母，仅有小写字母。
如果值为 capitalize，则要对某些字母大写，但是并没有明确定义如何确定哪些字母要大写，这取决于用户代理如何识别出各个“词”。

8、```background-size: cover;```
>把背景图像扩展至足够大，以使背景图像完全覆盖背景区域。
背景图像的某些部分也许无法显示在背景定位区域中。
contain:把图像图像扩展至最大尺寸，以使其宽度和高度完全适应内容区域。

参考文章： [CSS3 Background-size](http://www.w3cplus.com/content/css3-background-size)

9、```transform: scale(1.1); /* 放大1.1倍 */```

>scale(x,y)使元素水平方向和垂直方向同时缩放（也就是X轴和Y轴同时缩放）；
scale(<number>[, <number>])：提供执行[sx,sy]缩放矢量的两个参数指定一个[2D scale](http://www.w3.org/TR/SVG/coords.html#ScalingDefined)（2D缩放）。如果第二个参数未提供，则取与第一个参数一样的值。

参考文章： [CSS3 Transform](http://www.w3cplus.com/content/css3-transform)

10、```transition: all .07s ease;```

过渡是元素从一种样式逐渐改变为另一种的效果。
参考文章： [CSS3 Transition](http://www.w3cplus.com/content/css3-transition)