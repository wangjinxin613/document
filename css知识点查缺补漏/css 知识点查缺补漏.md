# css 知识点查缺补漏
#### 1. support, media的用法是什么？
@support主要用于检测浏览器是否支持css的某个属性，如果支持某个属性，就可以写一套样式，如果不支持某个属性，可以提供另外一套样式作为替补
基本语法如下：

```css
@support(prop:value){
/*自己的样式*/
}
@supports (display: flex) { div { display: flex; }}
```
[参考资料](cnblogs.com/yuxuan007/p/10892452.html)

media是媒体查询，可以针对不同的媒体类型定义不同的样式，在设计自适应的网页中会用到


```css
// 如果文档宽度小于 300 像素则修改背景颜色(background-color):
@media screen and (max-width: 300px) {
    body {
        background-color:lightblue;
    }
}
```
[参考资料](https://www.runoob.com/cssref/css3-pr-mediaquery.html)
#### 2. 1px、1rem、1em代表的含义

px是像素，是相对长度单位，像素是相对于显示器屏幕分辨率而言的。

em是相对长度单位，相对于当前对象内文本的字体尺寸，如当前对行内文本的字体尺寸为被人为设置，则相对于浏览器的默认字体尺寸。
em的值并不是固定的
em会继承父级元素的字体大小