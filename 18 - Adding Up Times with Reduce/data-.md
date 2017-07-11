# [data-*](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global_attributes/data-*)

```data-*``` 全局属性 构成一类名称为自定义数据属性的属性，允许通过脚本在HTML 和其 DOM 表示之间交换专有信息。所有这些自定义数据都可以通过属性设置的元素的 HTMLElement 接口来访问。  HTMLElement.dataset 属性可以访问它们。 * 可以使用遵循 xml名称生产规则 的任何名称来被替换，并具有以下限制：

- 该名称不能以xml开头，无论这些字母用于什么情况;
- 该名称不能包含任何分号 (U+003A)；
- 该名称不能包含A至Z的大写字母。

注意，HTMLElement.dataset 属性是一个 **StringMap**，并且自定义数据属性 data-test-value 可以通过 HTMLElement.dataset.testValue ( 或者是 HTMLElement.dataset["testValue"] )  来访问，任何破折号(U+002D) 都会被下个字母的大写替代(驼峰拼写)。
