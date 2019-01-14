1. css中div多个块级元素水平布局的方法: 使用float浮动布局.

技巧: 子元素加上display:float; 父元素使用clearfix清楚浮动
```css
.clearfix:after{
  clear:both;
  content: '';
  display: block;
}
```

2. 页面中元素的高度到底是由什么决定的:

块级元素由内部文档流元素的高度决定
内联元素的高度由字体的size决定,字体size和字体family有关联
