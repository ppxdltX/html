# 2020 年 8 月 7 日

> 笔记二：

## 规范

```
CSS属性书写顺序

建议遵循以下顺序:

1.布局定位属性: display / position/ float / clear / visibility / overflow (建议display第一个写)

2.自身属性: width/ height / margin/ padding / border / background

3.文本属性: color/ font / text-decoration/ text-align/ vertical-align/ white- space / break-word

4.其他属性(CSS3) : content/ cursor/ horder-radius/ box- shadow / text-shadow/ background:linear-gradient...
```

## 快捷键

```
单个tab，多个*几tab，父子>，同级+，类用.，id用#，顺序自增$,标签内内容{}
```

# 开头使用

```
*{
  margin:0;
  padding:0;
  box-sizing: border-box;
}
box-sizing: border-box;  // 变成css3模型,加了border和padding不需要减去值,内减模式
```

## BFC、IFC、GFC、FFC

```
BFC:          // 该容器布局 不会影响其他元素
选择器:{
  position:absolute/fixed;

}
```

## 元素层级关系

```
标准流 < 浮动 < 定位
定位中相对,绝对,固定,层级相同,html里谁在下谁更高
可以设置 z-index:整数;  取值越大 顺序约靠上 默认为0 必须配合定位否则无效
```

## 基础选择器

```
标签选择器：
直接使用标签(如：p,div)，所有标签都会被选择
类选择器：
使用.定义,元素加class="" 不能以数字和-开头,单个元素可以有多个类名,类名之间用空格隔开  类名可以重复在多个元素上使用
id选择器：
使用用#定义,元素上加id="",一个标签只能有一个id,id选择器只能使用一次
通配符选择器：
使用*定义，所有都会改变
```

## 复合选择器

```
后代选择器：  // 选择器与选择器之间空格隔开 父元素中的所有相同标签都会选择
父 子 ....{

}

子选择器:    // 父元素后加>表示选择子元素
父>子 {

}

兄弟选择器:
同级1 + 同级2{ // 选中的是紧跟在同级1后面的第一个同级元素,只选满足条件的

}

其他兄弟选择器:
同级1 ~ 同级2{  // 选中的是同级1后面所有符合条件的同级元素

}


并集选择器：  // 选多钟同级，最后一个不能加逗号
同级，同级 {

}

交集选择器:   // 选择器之间不用加空格 找到页面中既能被选择1选中又能被选择2选中的标签
选择1选择2{

}

伪类选择器： // 鼠标经过效果
选择器:focus{

}

结构选伪类选择器:
元素名:first-child{}       // 匹配父元素第一个子元素,并且是元素名的
元素名:last-child{}        // 匹配父元素最后一个子元素,并且是元素名的
元素名:nth-child(n){}      // 匹配父元素第n个子元素,并且是元素名的
元素名:nth-last-child(n){} // 匹配父元素倒数第n个子元素,并且是元素名的
括号中的n可以填公式:
2n、even         // 偶数         数字可换
2n+1、2n-1、odd  // 奇数          数字可换
-n+5             // 找到前五个     数字可换
n+5              // 从第五个往后找  数字可换

链接伪类选择器:
未访问过的 a:link{}---需要按照LVHA的顺序
           访问过的 a:visited{}
           鼠标经过的 a:hover{}
           鼠标按住没抬手的 a:active{}

伪元素选择器:
元素::before          // 在元素内部的最前面插入一个元素
元素::after           // 在元素内部的最后面插入一个元素
元素::first-letter    // 选择元素内第一个字母
元素::first-line      // 选择元素内第一行文本
必须设置content属性才生效 content='要加入的内容';
选择器::after{
  content="需要加入的内容"    // 格式
}
伪元素是默认行内元素

```

## 盒模型

```
属性:
box-sizing: content-box   // 默认值,盒模型是外扩的,width和height的值固定的,这时设置边框粗细与内边距等会向外扩张
box-sizing: border-box    // 内减模式,设置后width和height是确定整个模型的宽高,设置边框粗细与内边距会向内挤压内容
```

## 元素显示与隐藏

```

display:[]
block--显示
none--不占据空间隐藏
visibility:[];
visible--显示
hidden--占据空间隐藏

元素整体透明度:
opacity: ;    // 数值为0到1之间 1实体 0透明
```

## 元素溢出部分显示效果

```
overflow:
visible--默认值,溢出可见
hidden--溢出部分隐藏
scroll--无论是否溢出,都显示滚动条
auto--如果超出了才显示滚动条
```

## 元素显示模式转换

```
?{
  display: block;--显示元素,还可以转块级元素(可以设置宽高不能在一行)
  display: none;--隐藏元素
  display: inline;--转行级元素(不能设置宽高可以在一行)
  display: inline-block;--转行内块元素(可以设置宽高并在一行)
}
```

## 优先级(复合选择器会叠加)

```
继承和*选择器 0.0.0.0
标签选择器 0.0.0.1
类与伪类选择器 0.0.1.0
ID选择器 0.1.0.0
行内样式 1.0.0.0
!important 无限大不能提升继承 提升优先级到最高  !important写在属性后面 ;前面
```

## 表格样式

```
align--left,center,right表格相对周围对齐方式
border--粗细px 线条solid 颜色black三个值设置边框，默认""没有边框
cellpadding--像素值设置单元格边缘与内容的空白
cellspacing--像素值设置单元格之间的空白
width--像素值或百分比设置表格宽度
border-collapse:collapse;--每一个元素之间没有空隙
```

## 背景设置

```
background--背景
背景色及透明色设置
background-color:rgba(250,250,250,.2);--最后一个是背景透明度

background-image:url[];

background-size:[];--cover等比缩放填满盒子,还能设置数字+px,相对于目前宽高的百分比,contain将背景图等比放大,直到无法等比放大,就不再放大
transparent--透明色

background-repeat:[]--背景图片是否平铺
repeat-x--横向重复
repeat-y--纵向重复
repeat--横纵重复
no-repeat--不重复

background-position:[][];--位置设置(top|center|bottom|left|center|right)精确像素(第一个是 X 第二个是 Y),只写一个第二个默认垂直，


background-attachment--背景附着(是否随鼠标滚轮滚动，视差滚动)
background-attachment : scroll(随滚轮滚动) | fixed(不随滚轮滚动)

复合写法：background:color url repeat attachment position;(颜色 图片地址 平铺 滚动 位置)

background-size: ;   // 图片宽度与高度,只写一个数值是宽度,高度等比变化,可用px,对与父盒子的百分比,cover,完全覆盖父盒子,contain等比变化到盒子内的最大尺寸,
```

## div 文字样式

```

color: ;--颜色
font-size ;--尺寸,需要加单位
font-wight ;--粗细,正常normal或400,加粗bold或700
font-family ;--字体
font-style ;--字体风格(normal 正常，italic 斜体)
font:style weight size/line-height family;--复合写法(size 与 family 不能省)

```

## div 文本样式

```
text-align:left/center/right;--文字水平排列方式
text-align:center--在父元素上设置可以让父元素下的文本,span,a,input,img标签都居中对齐
text-decoration:none/underline(下划线)/overline(上划线)/line-through(删除线);--装饰文本 none可以用来清除a标签的下划线
text-indent:[]em ;--首行缩进 em就是文字大小
line-height: []px ;--文字行高,设置1.5就是字号的1.5倍,设置1可以取消上下行间距
文字垂直居中：行高=盒子高
```

## div 边框样式

```
border--[width粗细  dotted圆点虚线(dashed方块虚线)、solid实线  color颜色];--边框样式

border-top(bottom|left|right): [];--单边样式

border-collapse:collapse;--合并相邻的边框

border-radius: ;--设置四角角度(50%是圆)
border-radius:[],[],[],[]--顺时针上右下左(两个值是对角)
border-top-right-radius: []px;--右上
border-top-left-radius: []px;--左上
border-bottom-right-radius: []px;--右下
border-bottom-left-radius: []px;--左下
border-top: 0px solid black;--上
border-left: 0px solid black;--左
border-bottom: 0px solid black;--下
border-right: 0px solid black;--右
胶囊型:
首先盒子是长方形,其次border-radius取值是高度的一半

outline: none ; --边框轮廓属性


```

## 内外边距设置

```
*{margin:0;
  padding:0
  };--清除所有内外边距
margin--外边距
magin-top:[];
magin-left:[];
magin-bottom:[];
magin-right:[];
magin:0 auto;--水平居中

padding--内边距
padding-top:[];
padding-left:[];
padding-bottom:[];
padding-right:[];
padding:[] ;--一个值上下左右，两个值第一个上下第二个左右，三个值第一个上第二个左右第三个下，四个值上右下左顺时针
```

## 阴影(可用 hover)

```
盒子使用的阴影:
box-shadow:
h-shadow               // 必须写 水平偏移量 数字+px
w-shadow               // 必须写 垂直偏移量 数字+px
blur                   // 数字+px 可选模糊效果
spread                 // 数字+px 可选阴影尺寸
color                  // 可选阴影颜色
inset                  // 可选外部阴影变内部阴影
以上用空格隔开就可以使用,在浏览器检查工具中去修改

text-shadow:h-shadow，w-shadow，blur,color; // 文字使用的阴影
在所有的阴影中 多阴影中先写的阴影会压在后写的阴影的上面
```

## 浮动 浮动会脱离标准流,在标准流中不占位置,不能使用 margin: 0 auto;text-align:center;居中

```

float: left,right;--创建浮动
能够使图文环绕,块级元素同行(需要两个块级元素都设置一边)


清除浮动(四选一) 清除浮动带来的影响
1 clear:left，right，both(同时清除两侧);
在html父级元素内部的子元素最后一个后面,新建一个标签 如<div class="clearfix"></div>
在用class关联 然后在css中设置clear:both;必须是块级元素

2 overflow:auto;--在父级元素中设置

3 .clearfix::after {//在父元素中设,父元素中class后多加个调用clearfix
    content: "";
    display: block;
    height: 0;
    clear: both;
    visibility: hidden;
}
.clearfix:after { --ie6/7专用
  *zoom: 1;
}

4 .clearfix::before,  // 在父元素中设置 工作中常用!也能解决塌陷
  .clearfix::after {
    content: "";
    display: table;
}
.clearfix:after {
   clear: both;
}


.clearfix { --ie6/7专用
  *zoom: 1;
}
```

## div 弹性布局

```

display 在父元素上进行设置

display：flex;--默认所有子元素横着排列

flex-direction: []
row--横向排列
row-reverse--反方向横向排列
column--纵向排列
column-reverse--反方向纵向排列

justify-content:[];--根据设置方向均匀排版
space-between--边缘不留间隙
space-around--边缘留间隙
center--居中排版

align-items:center--根据设置方向垂直居中排版

flex-wrap:[];--在当前方向放不下元素是否换行
nowrap--不换行
wrap--换行

```

## div 定位方式 工作中一般子绝父相

```
position: static或 relative或 absolute或 fixe;
left: ;
right: ;
top: ;
bottom: ;
数字+px或者百分比 一般水平和垂直只用设置两个数值


static--静态定位[默认]

relative--相对定位[是相对于原来自己的位置]

absolute--绝对定位[不在占据位置.相对于它最近设置了的 relative 或 absolute 的祖先元素进行定位,父级都没有则依照浏览器窗口定位left就是距离左边多远right就是距离右边多远，其余一样,居中要设置left50% top50% 后再设置transform:translate(-50%,-50%)]

fixed--固定定位 位置参考的是浏览器,不占位置,会随着浏览器滚动一起往下

sticky--粘性单位 sticky生效的前提是，必须搭配top、bottom、left、right这四个属性一起使用，不能省略，否则等同于relative定位，不产生"动态固定"的效果。原因是这四个属性用来定义"偏移距离"，浏览器把它当作sticky的生效门槛。
```

## 伪类

```
选择器:hover{ ---表示鼠标移动到上方有的效果
color:[];--鼠标颜色
cursor:[];--鼠标形状  // default默认箭头,pointer点击小手,text选择文本的工字型,move十字光标,提示可以移动

}
```

## 过度效果 通常配合 hover 使用

```
transition:需要过度的属性 秒数 时间曲线 延时执行的时间;后两个可以省略
// 要在hover中去加transition ,所有的属性都能过度,举例为width和bgc 秒数自行设置,举例为5秒 过度多个属性需要中间加逗号 秒数要加单位
选择器{
  width: 500px;
  height: 600px;
  background-color: yellow;
  transition:all 5s;
}

选择器:hover{
  width: 1000px;
  background-color: red;
}

时间曲线的属性:
linear                       // 默认,匀速
ease                         // 逐渐慢下来
ease-in                      // 加速
ease-out                     // 减速
ease-in-out                  // 先加速后减速
cubic-bebezier(x1,y1,x2,y2)  // 自定义速度曲线
```

## 平面转换 2D 转换 通常配合 hover 使用

```
transform实现2D的属性: 多个属性同时设置中间用空格隔开
平移:translate()
                     -Y
上下左右使用的正负: -X   +X
                     +Y

transform:translate(X,Y);  // px和百分比都行
transform:translateX       // 单独设置
transform:translateY       // 单独设置

缩放:scale()
transform:scale(x,y);       // x y分别改变元素的宽高倍数
transform:scale(n);         // 只有一个值表示宽高同时缩放n倍
transform:scaleX(n);        // 改变元素的宽度
transform:scaleY(n);        // 改变元素的高度

旋转:rotate()
transform:rotate(数字deg);   // deg是角度顺时针是正数,逆时针是负数,旋转以后坐标轴也会跟着一起改变

倾斜:skew()
transform:skew(数字deg,数字deg);  // 分表是水平和垂直的倾斜角度,可以为正也可以为负,第二个数字不写默认为0

坐标轴的基准点:origin()
transform-origin:;           // 定义原点的位置在哪里,可以使用left,top,center,right,bottom,像素值,百分比,第一个数值是x轴第二个是y轴
```

## 3D 转换 通常配合 hover 使用

```
首先给父级设置3D效果的属性 透视 必须设置: 多个属性同时设置中间用空格隔开
3D模型是由多个元素构成,需要给这多个元素的父元素添加:
transform-style: preserve-3d
来使其变成一个真正的3D模型,这个模型会保留元素自己的转换轴坐标


perspective:数字px;        // 数值越小,变化越大,反之变化越小

transform实现3D的属性:
旋转:
transform:rotateX(数字deg);   // 沿着X轴
transform:rotateY(数字deg);   // 沿着Y轴
transform:rotateZ(数字deg);   // 沿着Z轴

位移:
transform:translateX();   // 沿着X轴
transform:translateY();   // 沿着Y轴
transform:translateZ();   // 沿着Z轴
```

## 动画 通常配合 hover 使用

```
@keyframes 动画名称{
  from{
                              // 开始
  }
  to{
                              // 结束
  }
或者百分比的形式 常用:
  0%{
                              // 开始
  }
  30%{
                              // 过程
  }
  60%{
                              // 过程
  }
  100%{
                              // 结束
  }
}

调用动画:
元素.{
  animation:动画名称 过度时间 速度曲线 动画次数 延迟时间; // 名称与时间必须设置,其他可以省略 多个属性中间空格隔开

  单独设置属性:
  animation-name: ;              // 动画名称
  animation-duration: ;          // 过度时间 默认0
  animation-timing-function: ;   // 速度曲线 默认ease
  animation-delay: ;             // 延迟时间 默认0
  animation-iteration-count: ;   // 动画次数 默认1 无限循环infinite
}
```

## 鼠标常见属性

```
元素.{
  cursor: ;    // default默认箭头,pointer点击小手,text选择文本的工字型,move十字光标,提示可以移动
}
```

## 精灵图 需要使用行内标签,将整个行内标签 css 改变背景图片

```
使用步骤：
1.创建一个尺寸与精灵图中的小图尺寸相同的盒子
2.将精灵图设置为盒子的背景图片
3.修改背景图位置
通过PxCook测量小图片左上角坐标,分别取负值设置给盒子的background-position:x y

```

## 字体图标

```
1.使用行内标签,引用样式表 link下载好的文件,与html放在同一个根目录
2.在行内标签中引用类目 引用一个iconfont一个图标名称复制过来
```

# a 标签可以去嵌套任意元素在其中,除了他自己

# css flex 布局

```
任何一个容器都能指定为flex布局:
display:flex;

flex在父元素常见的六个属性:
1. flex-direction:       // 设置主轴方向,元素根据主轴进行排列
row              // 默认从左到右
row-reverse      // 从右到左
column           // 从上到下
column-reverse;  // 从下到上

2. justify-content:      // 设置主轴上子元素的排列方式
flex-start      // 默认,从头部开始
flex-end        // 从尾部开始
center          // 在主轴居中对齐
space-around    // 平分剩余空间
space-between;  // 先两边贴边,再平分剩余空间

3. flex-wrap:            // 设置子元素是否换行
wrap         // 换行
nowrap;      // 不换

4. align-content:   // 设置侧轴上子元素排列方式,多行的(换行情况下的)
flex-start      // 默认,从头部开始
flex-end        // 从尾部开始
center          // 在侧轴居中对齐
space-around    // 平分剩余空间
space-between   // 先两边贴边,再平分剩余空间
stretch;        // 设置子元素高度平分父元素高度

5. align-items:          // 设置侧轴上子元素排列方式,单行的
flex-start      // 默认,从头部开始
flex-end        // 从尾部开始
center          // 在侧轴居中对齐
stretch;        // 拉伸 子盒子不能给高度

6. flex-flow:row wrap;  // 复合属性,相当于同时设置direction与wrap


flex在子元素中常见属性:
flex: 数字;    // 定义子元素来表示占多少剩余空间的份数

align-self:内部属性与之前的整体排列方式一样;   // 控制子元素在侧轴上的排列方式,允许单个项目与其他项目不一样的对齐方式,可以覆盖align-items属性,默认auto表示继承父元素

order:数字;    // 数字越小,排序越靠前,默认为0
```

## CSS3 媒体查询

```
内部样式表:
@media screen and (min-device-width:数字px) and (max-device-width:数字px) {

}
属性:
对比浏览器宽高
width:数字px;
hight:数字px;
对比屏幕宽高
device-width:数字px;
device-hight:数字px;

外部样式表：
<link rel="stylesheet" href="1.css" media="(min-device-width:数字px) and (max-device-width:数字px)">

```

## css3 中的渐变色

```

```

## css3 中的滤镜

```
filter常见属性:
filter: 函数();        // 例如 filter: blur(5px); blur是模糊
```

## css3 中的 calc 函数

```
例如width: calc(100% - 10px);   // 可以在括号内进行常规计算
```

## 移动端视口

```
使用理想视口:
ideal viewport
<meta name="viewport" content="width=device-width, initial-scale=1.0,maximum-scale=1.0,minimum-scale=1.0,user-scalable=no">
```

# 常见问题

```
一、外边框塌陷现象
互相嵌套的块级元素,子元素的margin-top会作用于父元素上
解决:
1.给父元素设置border-top或是padding-top,分离子父元素的margin-top
2.给父元素设置overflow:hidden
3.转换成行内块元素 display-inline-bolck
4.设置浮动  // 第四点一同解决

二、改变行内元素的上下位置
无法使用margin与padding的top和bottom改变
解决:
1.改变行高line-height

三、浏览器解析行内块与行内元素时,如果换行会使元素之间有空隙
解决:
使用浮动

四、子元素浮动,父元素不设置高度，后面的标准流盒子会受影响
解决:
.clearfix::before,  // 在父元素中设置 工作中常用!也能解决外边框塌陷
  .clearfix::after {
    content: "";
    display: table;
}
.clearfix:after {
   clear: both;
}

五、在浏览器当中文字与图片,或者行内块/行内元素与块级元素,不能垂直对齐,还有图片不能在块级元素中垂直居中
解决:
vertical-align:baseline    // 默认,沿基线对齐
               top         // 沿顶部对齐
               middle      // 沿中部对齐---最常用
               bottom      // 沿底部对齐
```

# 元素居中的多种方式

```
1.给元素本身设置
margin: 0 auto;    // 在 div,p,h 中使用 一般针对固定宽度的盒子,没有设置宽度会默认占满父元素的宽度

position: ;
left:50%;
top:50%;
transform:translate(-50%,-50%);  // 在使用了position后使用

2.给父级元素设置
text-align:center; // 在 文本,span,a,input,img 中使用
```

# less

```
@变量名: 值;        // 定义变量
```
