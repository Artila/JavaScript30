# [Element.getClientRects()](https://developer.mozilla.org/zh-CN/docs/Web/API/Element/getClientRects)

**Element.getClientRects()** 方法返回一个指向客户端中每一个盒子的边界矩形的矩形集合。 

### 语法

> var rectCollection = object.getClientRects();

#### 返回

返回值是ClientRect对象集合，该对象是与该元素相关的CSS边框。每个ClientRect对象包含一组描述该边框的只读属性——left、top、right和bottom，单位为像素，这些属性值是相对于视口的top-left的。即使当表格的标题在表格的边框外面，该标题仍会被计算在内。

起初，微软打算让这个方法给文本的每一行都返回一个TextRectangle，但是，CSSOM工作草案规定它应该给每个边框返回一个ClientRect。因此，对于行内元素这两个定义是相同的，但是对于块级元素，Mozilla只会返回一个矩形。（译者注：对于行内元素，元素内部的每一行都会有一个边框；对于块级元素，如果里面没有其他元素，一整块元素只有一个边框）。

当计算边界矩形时，会考虑视口区域（或其他可滚动元素）内的滚动操作.

返回的矩形不包括任何可能超出元素范围的子元素的边界。

对于HTML AREA元素、自身不做任何渲染的SVG元素、display：none元素和不直接渲染出来的任何元素，都将会返回一个空列表。

具有空边框的CSS盒子也会返回矩形，此时left、top、right和bottom坐标仍旧有意义。

小数级别的像素偏移是有可能的。



