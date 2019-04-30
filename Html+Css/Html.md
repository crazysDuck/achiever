### Web基础知识
主要浏览器:IE Firefox(火狐) Google Safari Opera
### Web标准构成
* 结构（Structure&emsp; )标准：用于网页元素进行整理和分类。
* 样式（Presentation)标准：版式、颜色、大小。
* 行为（Behavior&emsp; )标准：定义及交互的编写。
### HTML 定义 : hyperText markup language 超文本标记语言
### HTML 骨架格式
``` html
<html>                      根标签
	<head>                  头标签
		<title></title>     网页标题标签
	</head>
	<body>                  主体标签
	</body>
</html>
```
#### html关系
* 嵌套关系
``` html
<head>
	<title></title>
</head>
```
* 并列关系
``` html
<head></head>
<body></body>
```

&lt;!DOCTYPE HTML>指html5版本
### 常用标签
 1. 标题标签   h1~h6
``` html
<h1>一级标签</h1>   （一般页面中只出现一次）
<h2>二级标签</h2>
<h3>三级标签</h3>
<h4>四级标签</h4>
<h5>五级标签</h5>
<h6>六级标签</h6>
```
2. 段落标签  &lt;p&gt;&lt;/p&gt;
3. 水平分割线标签 &lt;hr /&gt;
4. 换行标签&lt;br /&gt;
5. 文本标签
 - 加粗   &lt;strong&gt;&lt;/strong&gt;  &lt;b&gt;&lt;/b&gt;
 - 斜体   &lt;em&gt;&lt;/em&gt;   &lt;i&gt;&lt;/i&gt;
 - 删除线   &lt;del&gt;&lt;/del&gt; &lt;s&gt;&lt;/s&gt;
 - 下划线    &lt;ins&gt;&lt;/ins&gt; &lt;u&gt;&lt;/u&gt;
 - 上标    &lt;sup&gt;&lt;/sup&gt;
 - 下标    &lt;sub&gt;&lt;/sub&gt;
6. 图像标签   &lt;img src="图像地址" /&gt;
 - &lt;img /&gt;属性


| 属性 | 单位 | 值 |
|:--:|:-:|:-:|
|src | URL | 路径 |
|alt | 文本 | 不能显示时替换文本 |
|title | 文本 | 鼠标悬停显示内容|
|width | 像素 | 图像宽 |
|height | 像素 | 图像长 |
|border | 数字 | 图像边框宽 |
7. 链接标签  

  &lt;a href="跳转目标" target="目标窗口弹出方式"&gt;文本&lt;/a&gt;
  target="self"  当前窗口打开     ="blank"在新的窗口打开
  - 外部链接  href="http://www.xxxxx.com"
  - 内部链接  href="xxx.html"
  - 空链接  href="#"
  - 图像做链接 &lt;a herf="#"&gt;&lt;img src="xxx,png" /&gt;&lt;/a&gt;   
* 相对路径
  - 同一级路径      &lt;img src="xxx.png" /&gt;
  - 下一级路径      &lt;img src="xxx/xxx.png" /&gt;
  - 上一级路径      &lt;img src="../xxx.png" /&gt;
8. 锚点链接
  * &lt;h3 id="xxx"&gt;标题&lt;/h3&gt;
  * &lt;a href="#xxx"&gt;&lt;/a&gt;
9. 特殊字符  


|  |空格符|&amp; nbsp;|
|  :--: | :-: | :-: |
|&amp;|和号|&amp; amp;|
|&lt;|小于号|&amp; lt;|
|&gt;|大于号|&amp; gt;|
   
   
10. 表格标签
```html
<table>
	<tr>
		<td>单元格内的文字</td>
		......
		......
	</tr>
	......
	......
</table>
```
|bgcolor|设置表格背景颜色|#000|
| :-: | :-: | :-: |
|border|设置边框|像素px|
|cellspacing|设置单元格与边框间距|像素px(默认2px)|
|cellpadding|设置内容与单元格间距|像素px(默认2px)|
|width|设置表格的宽|像素px|
|height|设置表格的高|像素px|
|align|设置表格在网页中的对齐方式|left center right|   

表头单元格标签 th    
用&lt;th&gt;&lt;/th&gt;代替&lt;td&gt;&lt/td&gt; （里面的文字居中加粗）     

表格标题  caption     
&lt;caption&gt;xxx&lt;/caption&gt;   

合并单元格   
跨行合并：rowspan=“合并单元格个数”
跨列合并：colspan=“合并单元格个数”   
&lt;thead&gt;&lt;/thead&gt; ：定义整个表格，放标题  （里面必须有&lt;tr&gt;）   
&lt;tbody&gt;&lt;/tbody&gt; ：定义表格的主格，放数据本体   
&lt;tfoot&gt;&lt;/tfoot&gt; ：定义表格的脚注   

11. 无序列表  
```html
<ul>
	<li>列表项1</li>
	<li>列表项2</li>
	<li>列表项3</li>
</ul>
```
&lt;ul&gt;&lt;/ul&gt;中只能嵌套&lt;li&gt;&lt;/li&gt;   
&lt;li&gt;&lt;/li&gt;里面可以容纳所有标签   

12. 有序标签   
```html
<ol>
	<li>列表项1</li>
	<li>列表项2</li>
	<li>列表项3</li>
</ol>
```
13. 自定义列表
```html
<dl>
	<dt>名词1</dt>
	<dd>名词1 解释1</dd>
	<dd>名词1 解释2</dd>
	...
	<dt>名词2</dt>
	<dd>名词2 解释1</dd>
	<dd>名词2 解释2</dd>
	...
</dl>
```
14. 表单   
<table align="center">
	<tr>
		<th>属性</th>
		<th>属性值</th>
		<th>描述</th>
	</tr>
	<tr>
		<td rowspan="9">type</td>
		<td>text</td>
		<td>单行文本输入框</td>
	</tr>
	<tr>
		<td>password</td>
		<td>密码输入框</td>
	</tr>
		<td>radio</td>
		<td>单选按钮</td>
	</tr>
	</tr>
		<td>checkbox</td>
		<td>多选按钮</td>
	</tr>
	</tr>
		<td>buttom</td>
		<td>普通按钮</td>
	</tr>
	</tr>
		<td>submit</td>
		<td>提交按钮</td>
	</tr>
	</tr>
		<td>reset</td>
		<td>重置按钮</td>
	</tr>
	</tr>
		<td>image</td>
		<td>图像形式的提交按钮</td>
	</tr>
	</tr>
		<td>file</td>
		<td>文件域</td>
	</tr>
	</tr>
		<td>checked</td>
		<td>checked</td>
		<td>定义选中控件默认选中项</td>
	</tr>
	</tr>
		<td>name</td>
		<td>用户自定义</td>
		<td>控件的名称</td>
	</tr>
	</tr>
		<td>value</td>
		<td>用户自定义</td>
		<td>控件内的默认文本值（需要手动删除）</td>
	</tr>
	</tr>
		<td>placeholder</td>
		<td>用户自定义</td>
		<td>控件内的默认文本值（自动删除）</td>
	</tr>
	</tr>
		<td>size</td>
		<td>正整数</td>
		<td>控件内在页面中的显示宽度</td>
	</tr>
	</tr>
		<td>maxlength</td>
		<td>正整数</td>
		<td>定义控件输入的最多字符</td>
	</tr>
</table>

 * 提高用户体验(当我们鼠标点到用户名上时，光标定到表单里面)        
  - 直接包括    
  &lt;label&gt;用户名：&lt;input type="radio" value="用户名"&gt;&lt;/label&gt;
 - 通过for和id控制   
   &lt;label for="nc"&gt;昵称：&lt;/label&gt;   
   &lt;input type="text" id="nc"/&gt;   
   readonly  只读属性，输入框内容不能更改   
   disabled  禁用，表单的值再提交时会被舍弃   
 * 文本域       
```html
<textarea cols="每行中的字符数" roes="显示的行数">
	文本内容
</textarea>
```   
 * 下拉列表   
 ```html
 <select>
	<option>选项1</option>
	<option>选项2</option>
	<option>选项3</option>
</select>
```   
默认选中   selected="selected"    
 * 表单域   
 ```html
 <form action="地址" method="提交方式" name="表单名">
	各种控件
</form>
```
 - 实现表单的分组   
   &lt;fieldset&gt;&lt;/fieldset&gt;分组表单控件   
   &lt;legend&gt;&lt;/legend&gt;为fieldset定义标题   
15. 分区元素
* 行内元素:在一行內允许显示多个元素的,称为行内元素.  
(Span,i,b,s,u,sup,sub,em,strong,del,a等)
* 块级元素:每个元素独占一行显示的,称为"块级元素".  
(div,p,h1~h6,ul,li,ol,form,address等)
* 行内块元素:可以设置宽高,并且能在同一行的元素.   
(img,input,button等)
