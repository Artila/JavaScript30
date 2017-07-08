# [contenteditable](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global_attributes/contenteditable)

全局属性**contenteditable**是一个枚举属性（enumerated attribute），表示元素是否可被用户编辑。 如果可以，浏览器会修改元素的部件（widget）以允许编辑。该属性必须是下面的值之一：

- true 或空字符串，表示元素是可编辑的；
- false 表示元素不是可编辑的。


如果没有设置该属性，其默认值继承自父元素。

该属性是一个枚举属性（enumerated one），而非布尔属性（Boolean one）。这意味着必须显式设置其值为 true、false 或空字符串中的一个，并且不允许简写为 ```<label contenteditable>Example Label</label>``` （注：这在大部分浏览器中是有效的）,正确的用法是``` <label contenteditable="true">Example Label</label>```。


# [document.execCommand](https://developer.mozilla.org/zh-CN/docs/Web/API/Document/execCommand)

当一个HTML文档切换到设计模式(designMode)时，文档对象暴露 execCommand方法，该方法允许运行命令来操纵可编辑区域的内容。大多数命令影响文档的选择（粗体，斜体等），而其他命令插入新元素（添加链接）或影响整行（缩进）。当使用 contentEditable时，调用 execCommand() 将影响当前活动的可编辑元素。

##**语法**

> bool = document.execCommand(aCommandName, aShowDefaultUI, aValueArgument)

##**返回值**

一个 Boolean ，如果是 false 则表示操作不被支持或未被启用。

##**参数**

**aCommandName**
&nbsp;&nbsp;&nbsp;&nbsp;一个 DOMString ，命令的名称。可用命令列表请参阅命令。

**aShowDefaultUI**
&nbsp;&nbsp;&nbsp;&nbsp;一个 Boolean 是否展示用户界面，一般为 false。Mozilla 没有实现。

**aValueArgument**
&nbsp;&nbsp;&nbsp;&nbsp;一些命令需要一些额外的参数值（如insertimage需要提供这个image的url）。默认为null。


##**常用命令**

**bold**
&nbsp;&nbsp;&nbsp;&nbsp;开启或关闭选中文字或插入点的粗体字效果。IE浏览器使用``` <strong>```标签，而不是```<b>```标签。

**italic**
&nbsp;&nbsp;&nbsp;&nbsp;在光标插入点开启或关闭斜体字。 (Internet Explorer 使用 EM 标签，而不是 I )。

**justifyCenter**
&nbsp;&nbsp;&nbsp;&nbsp;对光标插入位置或者所选内容进行文字居中。

**justifyLeft**
&nbsp;&nbsp;&nbsp;&nbsp;对光标插入位置或者所选内容进行左对齐。

**justifyRight**
&nbsp;&nbsp;&nbsp;&nbsp;对光标插入位置或者所选内容进行右对齐。

**underline**
&nbsp;&nbsp;&nbsp;&nbsp;在光标插入点开启或关闭下划线。
