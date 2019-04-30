### css样式书写位置
1. 行内式（内联式）   
   &lt;标签名  style="属性1:属性值1;属性2:属性值2;"&gt;内容&lt;/标签&gt;   
2. 内部式   
```html
<head>
	<style type="text/css">
		选择器 {
			属性1: 属性值1;
			属性2: 属性值2;
			属性3: 属性值3;
		}
	</style>
</head>
```   
3. 外部样式(外联式)
```html
<head>
	<link rel="stylesheet" type="text/css" href="文件路径"/>
</head>
```
### CSS样式选择器    

1. 类选择器     
  .类名 {   
	   属性1:属性值1;   
	   属性2: 属性值2;   
	   属性3: 属性值3;   
	}    
2. id选择器  
  #id名 {
		属性1:属性值1;   
	    属性2: 属性值2;   
	    属性3: 属性值3;  
  }  
3. 统配符选择器   
  \* {
	  属性1:属性值1;   
	  属性2: 属性值2;   
	  属性3: 属性值3; 
  }
4. 后代选择器   
.class h3 {
	属性1:属性值1;  
}   
5. 子选择器   
.class>h3 {
	属性1:属性值1;
}   
6. 交集选择器  
h3.class {
	属性1:属性值1;
}  
7. 并集选择器  
.class,
h3 {
	属性1:属性值1;
}  
8. 伪类选择器  
a:link  &nbsp;&nbsp;未访问的链接  
a:visited &nbsp;&nbsp;已经访问的链接  
a:hover &nbsp;&nbsp;鼠标移动到链接上
a:active &nbsp;&nbsp;选定的链接   
### 标签显示模式  
1. 块级元素   
常见的有&lt;div&gt;(典型)&lt;h1&gt;~&lt;h6&gt; &lt;p&gt; &lt;ul&gt; &lt;ol&gt; 等    
 * 独占一行
 * 宽度,高度,外边距和内边距可以控制  
 * 里面可以放行内元素和行内块元素
   * p 里面不能放div标签
   * h1~h6.dt里面不能放其他块元素标签   
2. 行内元素  
 常见的有&lt;span&gt; &lt;a&gt; &lt;strong&gt; &lt;i&gt; &lt;ins&gt; 等     
 * 相邻行内元素在一行上,一行可以显示多个   
 * 宽度,高度直接设置是无效的  
 * 默认宽度是它本身内容的宽度  
 * 行内元素之容纳文本和其他的行内元素  
   * 链接里面不能再放链接 
   * 特殊情况下a里可以放块级元素,把a转化成块级元素更安全  
3. 行内块元素  
&lt;img /&gt; &lt;input /&gt; 
 * 和相邻的行内(行内块)在一行上,但之间有缝隙,一行可以显示多个  
 * 默认的宽度是它本身的宽度
 * 高度,行高,外边距和内边距都可以控制  
### 标签显示模式转换   
* 块转行内: display:inline;  
* 行内转块: display:block;  
* 块,行内转行内块: display:inline-block   
### 三大特性  
1. 层叠  
样式冲突,遵循就近原则  样式不冲突,不会层叠  
2. 继承  
子标签会继承父标签的某些样式(颜色,字号) &nbsp;&nbsp;&lt;a&gt;特殊不继承    
(text-, font-, line-, color可继承)   
3. 优先级  
选择器相同,执行层叠   
选择器不同,就会会出现优先级   

   权重
	 * 权重计算   

	 |选择器|权重| 
	 | :--: | :--: |
	 |继承或者\*|0,0,0,0|
	 |标签选择器|0,0,0,1|
	 |类选择器|0,0,1,0|
	 |id选择器|0,1,0,0|
	 |行内样式|1,0,0,0|
	 |!important|无穷大|

	 * 权重叠加  

	 |选择器 | 权重 |
	 | :--: | :--: |
	 |div ul li |0,0,0,3|
	 |.nav ul li |0,0,1,2|
	 |a:hover|0,0,1,1|
	 |.nav a|0,0,1,1| 

### 字体  
1. 字体大小  
font-size: 20px;    &nbsp;&nbsp;单位:像素(px)   
2. 字体  
font-family: "宋体","微软雅黑","黑体"; &nbsp;&nbsp;多字体逗号隔开
3. 字体粗细  
font-weight: 400; &nbsp;&nbsp; normal(默认)==>400 bold(加粗)==>700    可写数字:100~900      
4. 字体风格  
font-style: normal; &nbsp;&nbsp;normal默认 italic斜体  
5. 简写
font:风格 粗细 大小/行高 字体;   
### 文本
1. 文本水平对齐  
text-align: left(左对齐)/right(右对齐)/center(居中)  
2. 行高   
line-height :24px;  &nbsp;&nbsp;行高等于盒子高可以让文本垂直居中,一般比字号大7,8像素   
3. 首行缩进  
text-indent: 2em; &nbsp;&nbsp;(em:当前单位的倍数)  
4. 下划线  
text-decoration: underline; &nbsp;&nbsp;none(默认)下划线 underline取消下划线  
### 背景 
1. 背景颜色  
background-color: red; &nbsp;&nbsp;transparent(默认):透明     
* 透明度  范围0~1
  background: rgba(0,0,0,0.4)  &nbsp;&nbsp;0.4可简写.4   
2. 背景图像  
background-image: url(图片路径);   
3. 背景图像大小  
background-size: xx%(宽) xx%(高)   
4. 背景平铺  
background-repeat: repeat; 

 | 值 | 结果 |
 | :--- | :--- | :--- |
 | repeat(默认) |在横向和纵向上平铺 |
 | no-repeat |不平铺 |
 | repeat-X | 在横向上平铺 |
 | repeat-Y | 在纵向上平铺 |   
5. 背景位置  
background-position: xx% xx%; &nbsp;&nbsp; 百分比/浮点数字和单位/方位名词:top,center,bottom,left,center,right   
6. 背景附着  
background-attachment: scroll; &nbsp;&nbsp;scroll(默认):图像随内容滚动  &nbsp;&nbsp;fixed:图像是固定的
7. 简写 
background: 颜色 地址 平铺 位置 滚动;
### 边框 
border: 宽度 样式 颜色;   
样式:none(默认)无 solid单实线 dashed虚线 dotted点线 double双实线    
可以单独设置top/bottom/left/right的边框
### 内边距  
一个值&nbsp;&nbsp;padding: 上下左右  
两个值&nbsp;&nbsp;padding: 上下 左右  
三个值&nbsp;&nbsp;padding: 上 左右 下  
四个值&nbsp;&nbsp;padding: 上 右 下 左   
### 外边距  
一个值&nbsp;&nbsp;margin9: 上下左右  
两个值&nbsp;&nbsp;margin9: 上下 左右  
三个值&nbsp;&nbsp;margin9: 上 左右 下  
四个值&nbsp;&nbsp;margin9: 上 右 下 左  
* 外边距合并
	* 上下两个元素(兄弟级)的上下外边距不是之和,而是取两个值中较大的值
    解决:尽量只给一个盒子添加margin
	* 嵌套(父子级)上下合并   
	 有嵌套关系且父元素没有上内边距和边框,发生合并,子元素的外边距跑到父元素处,取两者较大值
	 解决:可以为父元素定义上边框/内边距;可以为父元素添加overflow: hidden;    
### 浮动  (会脱离标准流)
float: none;  &nbsp;&nbsp;left左浮动 &nbsp;&nbsp;right右浮动  
浮动会脱标,为了不影响下面的标准流元素,给浮动元素添加一个标准流的父元素    
同一个父元素中的子元素要浮动都浮动    
* 清除浮动   
  1. 父元素没有高度  
	2. 盒子浮动
	3. 影响下面的布局    
* 额外标签法   
给最后一个浮动元素末尾添加一个空标签并给它添加clear: both;  
  left&nbsp;&nbsp;不允许左侧浮动
	right&nbsp;&nbsp;不允许右侧浮动
	both&nbsp;&nbsp;同时清除两边浮动   
* 父元素添加overflow
给父元素添加overflow: hidden;  &nbsp;&nbsp;hidden/auto/scroll   
* 使用after伪元素
```
.clearfix:after {
	content: "";
	display: block;
	height: 0;
	clear: both;
	visibility: hidden;
}
.clearfix {
	*zoom:1;  /*IE6,7专用*/
}
```   
* 使用双伪元素清除浮动
```
.clearfix:before,
.clearfix:after {
	content: "";
	display: table;
}
.clearfix:after {
	clear: both;
}
.clearfix {
	*zoom: 1;
}
```     
### 定位  
#### 边偏移   
通过top/bottom/left/right定义元素的边偏移   
#### 定位的模式  
1. 静态定位
相当于没有定位
2. 相对定位 relative (保留位置)  
相对于它原来的位置来说
3. 绝对定位 absolute (不保留位置)
相对于带定位的父辈元素,都没定位以浏览器为准    
  * 绝对定位盒子居中   

<table>
	<tr>
		<td rowspan="2">水平居中</td>
		<td>left: 50%;</td>
	</tr> 
	<tr>
		<td>margin-left: -(自身宽度的一半);</td>
	</tr>
	<tr>
		<td rowspan="2">垂直居中</td>
		<td>top: 50%;</td>
	</tr> 
	<tr>
		<td>margin-top: -(自身高度的一半);</td>
	</tr>
</table>  

  margin-top  可以用   
  transform: translateX(50%) translateY(50%);     

4. 固定定位  (完全不占位置)      
只认浏览器的可视窗口    
* 堆叠顺序 (只能用于相对定位,绝对定位,固定定位)   
Z-index:可以调整堆叠顺序(父元素内),数值越大越靠上    
### 显示和隐藏   
1. display &nbsp;&nbsp;(隐藏后不保留位置)   
display: none; &nbsp;&nbsp;隐藏对象   
display: block; &nbsp;&nbsp; 除了转换为块级元素,还有显示元素的意思    
inline-block, 浮动, 绝对定位, 固定定位都会改变display属性    
2. visibility &nbsp;&nbsp;(隐藏后不保留位置)
visibility: visible; &nbsp;&nbsp;对象可见   
visibility: hidden; &nbsp;&nbsp;对象隐藏    
3. overflow  溢出    

|属性|解释|
| :--- | :--- |
|visible|不剪切也不添加滚动条|
|hidden|超出部分隐藏|
|scroll|不管是否超出,总是显示滚动条|
|auto|超出自动显示滚动条,不超出不显示|
4. 溢出的文字省略号显示    
white-space: normal; &nbsp;&nbsp;默认   
white-space: nowrap; &nbsp;&nbsp;强制在一行内显示所有文本,直到结束或有br标签    
text-overflow: clip; &nbsp;&nbsp;不显示省略号,简单的裁剪   
text-overflow: ellipsis; &nbsp;&nbsp;文本溢出时显示省略号      


##### 鼠标样式   cursor
|属性值|结果|
| :--- | :--- |
|default|小白箭头|
|pointer|小手|
|move|移动|
|text|文本|
|not-allowed|禁止|
##### 输入框轮廓线   outline
outline: none;   
##### 防止拖拽文本域   
resize: none;    
##### 块元素水平居中   
盒子必须指定宽度   
margin: 0 auto;
##### 行内元素/行内块元素垂直对齐   (去除图片底部空白间隙)
vertical-align: baseline; 基线 (有间隙) 
vertical-align: top;顶线
vertical-align: middle;中线
vertical-align: bottom;底线    
##### 网页图标   favicon.ico图标
第三方网站:比特虫
在head之间引入   
&lt;link rel="shortcut icon" href="favicon.ico" /&gt;
### 过渡   (写到有变化的元素本身) 
transition: 要过渡属性(all 所有) 花费时间 运动曲线 何时开始;   
运动曲线: linear匀速 ease(默认)逐渐慢下来 ease-in加速 ease-out减速 ease-in-out先减后加      
### 旋转   transform  
|属性值|结果|
| :--- | :--- |
|rotate(180deg)|相对于自身中心|
|rotateX(180deg)|相对于自身垂直对中X轴|
|rotateY(180deg)|相对于自身水平对中Y轴|    
### 矩形四个圆角   
border-radius:左上角 右上角 右下角 左下角;

## Flex布局   
main axis  \[水平的主轴(x轴)]   
开始位置 main start &nbsp;&nbsp;结束位置 main end     
cross axis \[垂直交叉轴(y轴)]   
开始位置 cross start &nbsp;&nbsp;结束位置cross end   

1. flex-direction 决定主轴的方向(项目的方向)   

   属性值   
  * row(默认) &nbsp;&nbsp;水平方向 起点在左   
  * row-reverse &nbsp;&nbsp;水平方向 起点在右   
  * column &nbsp;&nbsp;垂直方向 起点在上   
  * column-reverse &nbsp;&nbsp;垂直方向 起点在下    
	
2. flex-wrap 排不下如何换行  

    属性值   
 * nowrap &nbsp;&nbsp;不换行   
 * wrap &nbsp;&nbsp;换行 第一行在上   
 * wrap-reverse &nbsp;&nbsp;换行 第一行在下  
3. flex-flow   
flex-direction和flex-wrap的缩写   

4. justify-content  主轴上的对齐方式  

   属性值 
 * flex-start &nbsp;&nbsp;左对齐
 * flex-end &nbsp;&nbsp;右对齐
 * center &nbsp;&nbsp;居中
 * space-between &nbsp;&nbsp;两端对齐,项目间间隙相等   
 * space-around &nbsp;&nbsp;项目两侧间隙相等,靠边只有一半   

5. align-items 在交叉轴上的对齐方式     

   属性值
 * flex-start &nbsp;&nbsp;在交叉轴的起点对齐
 * flex-end &nbsp;&nbsp;在交叉轴的终点对齐   
 * center &nbsp;&nbsp;在交叉轴的中点对齐
 * baseline &nbsp;&nbsp;项目的第一行文字的基线对齐   
 * stretch(默认) &nbsp;&nbsp;未设高度或auto,占满容器高度   

6. align-content 多根轴线的对齐方式,只有一根不起作用   
 
   属性值   
 * flex-start &nbsp;&nbsp;与交叉轴的起点对齐   
 * flex- end &nbsp;&nbsp;与交叉轴的终点对齐  
 * center &nbsp;&nbsp;与交叉轴的中点对齐   
 * space-between &nbsp;&nbsp;与交叉轴的两端对齐,中间间隔相等   
 * space-around &nbsp;&nbsp;每个轴线两侧距离相等,靠边只有一半   
 * stretch(默认) &nbsp;&nbsp;轴线占满整个交叉轴   
7. order 项目的排列顺序 
 order: 0; &nbsp;&nbsp;默认0    
8. flex-grow  放大的比例   
 flex-grow: 0; &nbsp;&nbsp; 默认0  有剩余空间也不放大   
9. flex-shrink  缩小的比例   
flex-shrink: 1; &nbsp;&nbsp; 默认1 剩余空间不足,项目缩小   
10. flex-basis 在分配剩余空间钱,项目占据的主轴空间  
flex-basis: 0; &nbsp;&nbsp;默认0   
11. 缩写  flex   
flex-grow,flex-shrink.flex-basis的缩写   
默认: 0 1 auto; &nbsp;&nbsp;后两个属性可选   
#### Flex子项  
1. align-self 单个项目与其他项目有不一样的对齐方式, 覆盖align-items   

   属性值
 * flex-start &nbsp;&nbsp;在交叉轴的起点对齐
 * flex-end &nbsp;&nbsp;在交叉轴的终点对齐   
 * center &nbsp;&nbsp;在交叉轴的中点对齐
 * baseline &nbsp;&nbsp;项目的第一行文字的基线对齐   
 * stretch(默认) &nbsp;&nbsp;未设高度或auto,占满容器高度    
