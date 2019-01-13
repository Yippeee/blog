# HTML常用标签的简介

### a
anchor 锚元素
a标签用于创建一个到其他网页、文件、同一页面内的位置、电子邮件地址或任何其他URL的超链接。
其中a标签常用的属性有：
**download**
此属性指示浏览器下载URL而不是导航到它，因此将提示用户将其保存为本地文件。
**href**
包含超链接指向的URL或URL片段。
href有很多种使用方法：
1. 创建一个电话连接： href="tel:+491570156"
2. 创建一个邮件连接： href="mailto: 11@cc.com"
3. 在本页面的跳转： href="\#xxx" 在加上\#的href中，页面只会在本页面跳转。同时注意一点，*页面会跳转*
4. 连接到外部的地址: 
> 常见情况：href="http://www.mozilla.com/" 直接跳转到对应的地址，
> 如果没有加上http:协议名，浏览器会自动加上当前页面的协议继续跳转。
> 例如href="//www.mozilla.com/"，就会取决于当前页面的协议
> 假如当前界面是pp.com/example
> href="aa",就会跳转至 pp.com/example/aa
> href="/aa",就会跳转至 pp.com/aa

	**target**
	该属性指定在哪个iframe相应：
	_self: 当前页面加载，即当前的响应到同一HTML 4 frame（或HTML5浏览上下文）。此值是默认的，如果没有指定属性的话。
	_blank: 新窗口打开，即到一个新的未命名的HTML4窗口或HTML5浏览器上下文
	_parent: 加载响应到当前框架的HTML4父框架或当前的HTML5浏览上下文的父浏览上下文。如果没有parent框架或者浏览上下文，此选项的行为方式相同_self。
	_top: IHTML4中：加载的响应成完整的，原来的窗口，取消所有其它frame。 HTML5中：加载响应进入顶层浏览上下文（即，浏览上下文，它是当前的一个的祖先，并且没有parent）。如果没有parent框架或者浏览上下文，此选项的行为方式相同_self

> 这里就可以发现a标签怎么都会跳转，无论是在当前界面还是跳转去其他界面，那怎么做一个不跳转的A标签呢。这里就可以使用JavaScript伪协议。
> ```href="javascript:;"```
> 让a点了之后页面不做任何动作。（感觉很无聊~）
-----------

### iframe
iframe的作用就是用于嵌套界面（现在很少使用了..）
其中的name是用来a 标签跳转的情况下使用的
```html
<iframe src="https://www.baidu.com" name="xxx"></iframe>
```

### form
表示了文档中的一个区域，这个区域包含有交互控制元件，用来向web服务器提交信息。
主要的属性有:
1. action: 表示form处理信息使用的URL,但是也会被form中的button和input标签中的formaction属性覆盖
2. autocomplete: form中的input是否有默认值,会不会被浏览器自动补全.同时这个也是可以被重载覆盖掉的
3. method:form表单具体使用哪一种HTTP方式提交表单,就是由method来决定的

### input
1. type: 
	input的值和它的type有很大的影响,先看下input有哪些type
	- button 按钮
	- CheckBox 复选框
	- radio 单选框
	- file 文件
	- date 日期
	- color 颜色
	- password 密码
	...
2. accept; 如果该元素的 type 属性的值是file,则该属性表明了服务器端可接受的文件类型；
3. autocomplete: 这个属性表示这个控件的值是否可被浏览器自动填充。
4. disabled: 这个布尔属性表示此表单控件不可用
5. placeholder 提示用户输入框的作用
6. readonly 这个布尔属性用于指明用户无法修改控件的值

### table
table现在的很多属性都不推荐使用,因为很多属性在table中的只是对样式对选择.HTML标签应该更加的语义化,不要去承担样式的作用.
那么就说下table应该怎么使用:  

1. thead: 表头
2. tfoot: 表尾
3. tbody: 表的内容
4. tr: row表示一行
5. th: 表格的头部 table heard
6. td: 表格的数据 table data

除此之外还可以使用colgroup进行分组.
