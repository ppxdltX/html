### 注释快捷键

```
ctrl+/   单行
shift+alt+a  多行

```

# 求职要求

```
1.计算机基础扎实，熟悉常见的数据结构、算法和设计模式;
2.理解并掌握JavaScript语言核心技术DOM、BOM、Ajax、JSON等(含ES6);
3.对 Javascript 框架应用(如 React/Vue/jQuery 等)有一定的经验；
4.对 CSS/Javascript 性能优化、解决多浏览器兼容性问题有一定的经验优先;
5.熟悉JSP/python/php/Node.js或其他一门后台技术;
6.了解常见前端开发框架，对前后端联合开发的技术原理有全面了解；
掌握常见网络协议和相关的其他底层网络协议的全面知识。
7.具备跨浏览器、跨终端的前端开发经验优先;熟悉 React、Webpack、Babel 等技术原理者优先;
```

## 开头使用

```
window.addEventListener('load', function(){})
```

## 立即执行函数(不需要调用.立马执行的函数,创建独立作用域以避免命名冲突)

```
写法:
1. (function(){

})()   // 第二个小括号可以看做调用函数,加入实参

2. (function(){

}())   // 第二个小括号可以看做调用函数,加入实参
```

### 行内设置弹出

```
onclick="alert()"
```

### 弹出输出、用户输入、控制台输出

```
alert()
prompt()
console.log()
```

### 变量、赋值、输出结果

```
var ??? = 10;
console.log()  / alert()  /  prompt()
```

### 临时变量

```
var temp;
```

### 数字型

```
数字前加0是 八进制
0~9 a~f 数字前加0
x  十六进制
var(Number.MAX_VALUE); 最大值
var(Number.MIN_VALUE); 最小值
Infinity 无穷大
-Infinity 无穷小

```

### 转义符 都用\开头 都写道引号里面

```
\n 换行
\t 缩进
\b 空格
输入符号
\\ 斜杠
\' 单引号
\" 双引号

```

### 检测、检测获取字符串长度

```
alert(内容.length);
console.(typeof 内容);
```

### 转换为字符串、数字、布尔、数据类型

```
内容.toString();
String(内容)
(内容 + '') 常用

parseInt(内容) 取整，不四舍五入，会去掉数字后面的字母
parseFloat(内容) 有小数
Number(内容)
(内容 - * / 0/) 隐式转换

Boolean(内容) 代表空，否定会转换为false 其余转为ture
```

### 运算符、递增递减（递增减不能加数值）、比较运算符、逻辑运算符

```
+-*/ %取余

变量++ -- 前置递增(递减)  先运算原值 后自加1
++ --变量 后置递增(递减)  先自加1 后运算

<= , >= , == , !=不等于 , !==,===全数值数据类型等于 ，一般等于会将字符串转为数字类型
【=,+=,-=,*=,/=,%=赋值 ==判断 ===全等】

&& 逻辑与 两者缺一不可
短路运算 123 && 456 表达式1为真则返回表达式2 反之返回1 0,null, underfined,NaN都为假
|| 逻辑或 两者其一对就对
表达式1为真返回1 表达式1为假返回2
! 取反符

```

### 流程控制 if 分支、三元表达式、switch 分支

```
if(条件表达式真或假){
    执行语句
}
    else if(条件){
        执行语句
    }
    else if(条件){
        执行语句
    }
     else if(条件){
        执行语句
    }
    else {
        执行语句
    }

三元表达式:
条件表达式真或假 ? 真返回1 : 假返回2 ;

switch(表达式){
    case value1:
    执行语句1;
    break;
    case value2:
    执行语句2;
    break;
    default:
    执行最后语句;

}
```

### for 循环、while 循环、do while 循环

```
for(i = 初始量; i <>= 终止量; i++ 如何变化){
    循环体
}
初始量，终止条件，按照什么条件循环

var ???
while(条件ture or false){
循环体
???++
}

do{
循环体
}while(条件)
与 while 的区别是先循环一次再判断是否符合条件

continue 退出单次循环
break 退出循环
```

### 数组、新增元素、数组扩容(追加)、冒泡排序

```
var 数组名称 = new Array();括号内一个数字代表长度，两个以上代表添加数组元素
或
var 数组名称 = [];

数组名[索引号];   --索引号从0开始

遍历(每个元素访问一次)
for (var i < 0; i < ?; i++)

数组名称.length = 一共多少个元素;

追加：
数组名称[索引号] = 追加元素;(如果原来索引号就有元素是替换)

不能直接给数组赋值(=) 赋值需要将被赋值的元素放前面

冒泡排序：两层for循环，内层交换次数=索引长度-交换趟数-1;
```

### 函数

```
函数名需要为动词,后面必须跟小括号
function 函数名(变量的名称1，变量的名称2){
    函数体:需要重复使用的代码
}
函数名(变量的值1,变量的值2);

arguments 能够传递所有实参
```

### 对象、遍历对象

```
三种方法创建
1.利用对象字面量
var 对象名称{
    属性1名称:内容,
    属性2名称:内容,
    属性3名称:内容,
方法:方法名称: 函数(){
        函数内容
    }
}；

2.new Object创建对象
var 对象名称 = new Objtect();
对象名称1.属性名称 = 内容;
对象名称2.属性名称 = 内容;
方法名称.属性名称 = function(){};

调用:
1.对象名称.属性名称;
2.对象名['属性名];
3.对象名称.方法名称();


3.构造函数
function 构造函数名 首字母大写(){
    this.属性名称 = 内容;
    this.方法名称 = function(){}
}
调用:
var 对象名称 = new 构造函数名();

遍历对象:(变量常用k与key)
for (var 变量 in 对象){
    console.log(变量); 输出得到属性名
    console.log(对象[变量]); 输出得到属性值
}

```

### 在 MDN 手册中查询:Math 对象，Date 对象,

```
Math.PI         // 圆周率
Math.floor ()   // 向下取整
Math.ceil()     // 向上取整
Math.round()    // 四舍五入版就近取整 注意-3.5结果是-3
Math.abs ()     // 绝对值
Math.max()/.min()  // 求最大和最小值
Math.random()   //返回一个伪随机小数

Date() 是一个构造函数,只能使用new 调用
Date.now()H5新增 需考虑兼容
或+new Date() 获得1970至今总毫秒数,也就是当前系统时间毫秒数
倒计时中使用时间戳计算:
var nowtime = +new Date();
var futuretime= +new Date('年-月-日 时:分:秒'); //需要的将来的时间格式
var times = (futuretime - nowtime)/1000; //总秒数
var d = parseInt(times / 60 / 60 / 24); // 计算天数
var d = d < 10 ? '0' + d : d;
var h = parseInt(times / 60 / 60 % 24); // 计算小时
var h = h < 10 ? '0' + h : h;
var m = parseInt(times / 60 % 60); // 计算分数
var m = m < 10 ? '0' + m : m;
var s = parseInt(times % 60); // 计算当前秒数
var s = s < 10 ? '0' + s : s;
```

### 检测是否为数组、添加与删除数组元素、数组排序、数组索引、数组转化为字符串

```
是否为数组:
1.数组名 instanceof Array
2.Array.isArray(需要检测的参数)需考虑兼容

添加与删除:
1.数组名.push()     // 在数组末尾添加元素
2.数组名.unshift()  // 在数组开头添加元素
(添加后返回数组长度,删除后返回删除元素)
1.数组名.pop()      // 在数组末尾删除一个元素
2.数组名.shift()    // 在数组开头删除一个元素

反转数组:
数组名.reverse();

冒泡排序:
数组名.sort(function(a.b){
    return a - b;   //  升序排列
    return b - a;   //  降序排列
});

数组索引,返回该元素的索引号:
1.数组名.indexOf(需要索引的元素);  // 只返回第一个满足条件的索引号,在数组中找不到元素返回 -1
2.数组名.lastindexOf(需要查找的元素);  // 从后往前查找,只返回第一个满足条件的，找不到返回-1

数组转化字符串:
数组名.join(分隔符号，不输入默认逗号)；

其他:
数组名.concat()       // 连接两个或者多个数组不影响原数组，返回一个新数组
数组名.slice(截取开始数,结束数)        // 数组截取，返回截取后新数组
数组名.splice(删除开始数,结束数)       // 数组删除，返回删除后新数组，会影响原数组
```

### 返回字符串位置、根据位置返回字符、字符串操作方法

```
返回字符串位置:
1.字符串名称.indexOf('需要返回的内容' , 起始位置);  // 只返回第一个满足条件的索引号  起始位置可写可不写，找不到返回-1
2.字符串名称.lastindexOf(需要查找的内容);  // 从后往前查找，找不到返回-1

根据位置返回字符串:
1.字符串名称.charAt(索引号位置);
2.字符串名称.charCodeAt(位置);  // 返回索引号的字符的ASCII值,用于判断用户按下哪个键
3.str[位置]    // h5新增 需要考虑兼容

拼接字符串:
字符串名称.concat('需要拼接的字符')
截取字符串:
字符串名称.substring(开始值,结束值 不输入默认到最后一位)  // 不接受负值
替换字符串:
字符串名称.replace('被替换的','替换的')  // 只会替换第一个字符
字符转化为数组:
字符串名称.split('=或其他符号')    // 用来分隔的符号

```

# DOM 文档对象模型 主要重点：创建，增删改查，属性与事件操作

### 顶级对象为 document,即文档模型,操作的是页面元素,标准是 W3C 规范

```
DOM将这些内容都看为对象:
1.文档:一个页面就是一个文档，用document表示
2.元素:页面中所有标签都是元素，用element表示
3.节点:网页中所有内容都是节点(标签、属性、文本、注释等),用node表示

获取元素:
1.使用id获取 document.getElementById(区分大小写的ID，字符串格式)
2.使用标签获取 document.getElementsByTagName() // 伪数组形式存储
3.获取父元素中所有指定签名的子元素
第一步 document.getElementById()  //获取元素
第二部 元素名.getElementsByTagName() //获取子元素
// 必须是单个对象,必须指明是哪一个元素,一般document获取返回为伪数组形式,需要指定是伪数组中的具体元素,获取时不包括父元素自己

4.使用类获取 h5新增需注意兼容
document.getElementsByClassName()

5.无限制获取 h5新增需注意兼容
document.querySelector()     //相同元素中第一个
document.querySelectorAll()  //相同元素所有,元素需要加上元素类型符号 类.  id#

6.获取body与html
var bodyEle = document.body;
var htmlEle = document.documentElement;

7.**事件**
var 变量 = document.getElementById('事件触发的对象');  //1.获取事件源
事件触发对象.事件触发条件 = function(){  //2.事件类型与处理
    事件
}

常见的鼠标事件
onclick     ---左键点击触发
mouseenter  ---鼠标经过触发,不会被冒泡现象触发,常用
mouseleave  ---鼠标离开触发,常用
onmouseover ---经过触发,会被冒泡现象触发
onmouseout  ---离开触发
onfocus     ---获得鼠标焦点触发
onblur      ---失去鼠标焦点触发
onmousemove ---鼠标移动1px就触发
onmousedown ---鼠标按下触发
onmouseup   ---鼠标弹起触发

在addEventListener函数中,需要去掉on使用

8.改变元素的内容
元素名.innerText  // 更换内容去除html标签与空格和换行
元素名.innerHtml  // 常用 更换内容保留html标签与空格和换行
输入框.value      // input值更换需要使用
this.disabled = true   // 触发按钮失效,函数中谁调用this指向谁
this.style.需要改的样式 = '样式的内容'  // 需要改的样式使用驼峰命名如fontSize  backgroundColor
this.className  = '修改的类'  //  覆盖使用的类
this.className  = '第一个类 第二个类'  //  不覆盖的方法


9.**遇到点击转换两个状态时做法**
利用一个flag变量来判断值,是0时切换一种状态,是1时切换另一种
var flag = 0;
元素名.onclick = function() {
       if (flag == 0){
           改变内容;
           flag == 1;  // 重新赋值
       }
       else{
           改变内容;
           flag == 0;  // 重新赋值
       }
   }


```

### 排他思想(算法)

```
第一步:获取所有事件源
第二布:使用for循环将所有获取的源绑定事件
第三步:在for循环内嵌套一个for循环重置至初始效果
第四步:实现this事件的单个效果
```

### 全选功能

```
利用this.checked   // 得到当前复选框的选中状态true、false

var 变量 = document.getElementById('全选按钮')
var 变量= document.getElementById('父级元素').querySelectorAll('复选按钮')
全选按钮.onclick = function() {
    for (var i = 0; i < 复选按钮.length; i++) {
        复选按钮[i].checked = this.checked;
    }
}
for(var i=0;i<复选按钮.length;i++){
    复选按钮[i].onclick = function(){
        var flag = true;
        for(var i=0;i<复选按钮.length;i++){
            if(!复选按钮[i].checked){
                flag = false;
                break;
            }
        }
        全选按钮.checked = flag;
    }
}
```

### 自定义属性

```
自定义属性需要data- 开头

设置属性:
在元素中直接设置 <div = data-index"0"> </div>
在js中设置 div.getAttribute('index',改后值);

获取属性值:
不是元素自带的属性,如id class等,而是程序员定下的新属性如index = "1"等叫做自定义属性
<div id ="xxx" class="zzz" index = "yyy">
var div = document.querySelector('div')
自带属性:console.log(div.id);
自定义属性: console.log(div.getAttribute('index'));
h5新增获取自定义:div.dataset.index;

更改属性值:
自带属性:div.id = '改后值';    div.className = '改后值';

给元素添加自定义属性 元素.setAttribute('index',改后值);
获取自定义属性:div.getAttribute('index');

删除自定义属性:div.removeAttribute('index',改后值);

```

### 节点操作

```
节点类型 nodeType 元素节点为1,属性节点为2,文本节点为3
节点名称 nodeName
节点值 nodeValue

获取父节点、子节点
元素.parentNode   // 找不到返回full
!不常用 元素.childNodes   // 会得到所有节点,元素文本等
元素.children     // 获取所有子元素节点

获取第一个和最后一个子节点
元素.firstElementChild   // 返回第一个子元素节点 ie9以上兼容
元素.lastElementChild    // 返回最后一个 ie9以上兼容
常用 元素.children[0];   // 第一个
     元素.children[元素.children.length-1];  //最后一个

获取兄弟元素节点
元素.nextElementSibling       // 下一个元素节点 ie9以上兼容
元素.previousElementSibling   // 上一个元素节点 ie9以上兼容

动态创建、插入节点
创建:
var 变量 = document.createElement('需要的元素')
插入:
node.appendChild(变量)   // node父级  child子级 添加时不用''插入到父级元素下
元素.inserBefore(child,指定元素)   // 插入到指定元素前

删除节点
元素.removeChild(child)   // 删除子元素

复制节点
元素.clnoeNode(true);   // 括号为空或者是false 只复制标签不复制内容
```

### 方法监听注册事件(可以同一元素添加多个事件)

```
addEventListener()   // ie9以前不兼容,可使用attachEvent()替代
元素.addEventListener('字符串类型的事件',function(){
    执行的事件
} ,[可选参数 布尔值默认flase])   //在事件类型字符串中不需要on而且要加''

移除注册事件:
元素.addEventListener('事件',函数名)
function 函数名(){
    执行的事件
    元素.removeEventListener('事件',函数名)
}


```

### 冒泡与捕获

```
捕获与冒泡阶段:
addEventListener() 中的第三个参数true是捕获阶段从大到小,false与不输入是冒泡顺序,从小到大,onblur、onfocus、onmouseenter、onmouseleave没有冒泡阶段

事件对象:
event 写到侦听函数小括号里,有了事件才会存在,是事件相关数据的集合,比如鼠标事件中的相关信息有鼠标坐标等,键盘事件中有判断用户按下什么键等,还可以写成evt,e ie9以下用window.event
e.target    // 触发事件的元素 this则是返回绑定事件的元素ie9以下不兼容
e.eype      // 事件的类型
e.preventDefault();   // 阻止默认行为,如让链接不跳转或按钮不提交

阻止冒泡事件:
e.stopPropagation();  // ie9以下不兼容

事件委托:
给父节点添加侦听器,利用冒泡特性影响每一个节点,之后使用e.target进行下一步操作

```

### 禁用鼠标右键菜单、禁止选中文字

```
菜单document.addEventListener('contextmenu',function(e){
    e.preventDefault();
})

文字document.addEventListener('selectstart',function(e){
    e.preventDefault();
})
```

### Mousemove 鼠标事件

```
MouseEvement:
e.clientX     // 返回鼠标相对于浏览器窗口可视区的X坐标
e.clientY     // 返回鼠标相对于浏览器窗口可视区的Y坐标
***e.pageX       // 返回鼠标相对于文档页面的X坐标 ie9+支持***
***e.pageY       // 返回鼠标相对于文档页面的Y坐标 ie9+支持***
e.screenX     // 返回鼠标相对于电脑屏幕的X坐标
e.screenY     // 返回鼠标相对于电脑屏幕的Y坐标

鼠标移动图片跟随案例:
1.获取图片
2.利用e.pageX，Y获取鼠标位置 document.addEventListener('mousemove',function(e){
    var x = e.pageX
    var y = e.pageY
    图片.style.left = x + 'px';
    图片.style.top = y + 'px';
})
3.
```

### 键盘事件

```
keyup      // 松开按键触发
keydown    // 按下按键触发
keypress   // 按下按键触发 但是不识别功能键ctrl shift等

e.kcyCode返回键盘按下按键的ASCII码值
keyup与keydown不区分字母大小写
keypress区分字母大小写
```

### 搜索框等获得鼠标焦点方法

```
1.获取搜索框
2.写入判断条件
3.满足条件使用 元素名.focus();
```

# BOM 浏览器对象模型

### 顶级对象为 window,即浏览器对象模型,操作的是浏览器的交互,标准暂无统一

```
页面加载:
window.onload = function(){} // 文档内容加载完成后才触发的事件,只能使用一个
window.addEventListener('load',function(){})  // 无限制的使用方式
documen.addEventListener('DOMContentLoaded',function(){}) // 文档内容除了css图片flash等加载完成后就触发的事件,适用于图片较多的网站 i9以下不兼容

窗口大小事件:
window.onresize = function(){}
document.addEventListener('resize',function(){})
window.innerWidth   // 当前窗口宽度
window.innerHeight  // 当前窗口高度

计时器:  建议给定时器前加var起名
var timer1 = setTimeout(function(){}, 延迟多少毫秒调用函数);  // function可以用函数名去替换
var timer2 = setInterval(function(){}, 间隔多少毫秒反复调用函数)
停止定时器:
clearTimeout(定时器id);
clearInterval(定时器id);
在setInterval中,如果需要该定时器立刻执行内部函数,要对function进行封装,封装内最后必须有return来返回值,在调用时函数名后必须加(),如果带括号则先执行函数,将返回值作为参数,不带括号会被视为函数指针,根据设定的时间延迟执行

this指向问题:
在一般情况下,谁调用的函数this就指向谁
全局作用域与普通函数还有定时器中的this指向的都是window

location对象:
用以获取或设置、解析URL,URL是统一资源定位符,每个文件都有的唯一URL,包含的信息有文件位置以及浏览器如何处理
protocol       // 通信协议 常用http,ftp,maito等
host           // 主机(域名) www.wangzhi.com等
port           // 端口号 可选,省略时使用默认,如http默认端口80
path           // 路径 由零或者多个/隔开的字符串,表示主机上的目录或者文件地址
query          // 参数 以键值对的形式通过&隔开
fragment       // 片段 #后面内容,常见于锚点链接
常用的location
location.href         // 获取或设置URL
location.host         // 返回主机(域名)
location.port         // 返回端口号,未写返回空白字符串
location.pathname     // 返回路径
location.search       // 返回参数
location.hash         // 返回片段
location方法:
location.assign()     // 和href一样也能跳转页面 可以计入浏览历史和后退
location.replace()    // 替换当前页面 不能计入浏览历史和后退
location.reload()     // 重新加载页面和F5一样 括号内为true是强制刷新

navigator对象:
navigator.userAgent   // 判断用户使用的是什么终端

history的方法:
history.back();       // 后退功能
history.forward();    // 前进功能
history.go();         // 括号中输入1是前进一个页面 -1是后退一个页面
```

### js 同步异步

```
执行顺序不同:
同步按照代码顺序执行
异步按照代码执行事件的时间长短顺序执行
先执行执行栈中的同步任务,将执行栈中的异步任务放入任务队列中,执行完同步任务后找到异步任务再放入执行栈中执行
多个异步任务时先放入异步进程处理,完成事件才放入任务队列
执行栈会反复进入任务队列搜索是否有任务执行,这叫作事件循环
```

### 元素常见获取

```
元素偏移量offset
常用属性:
元素.offsetParent      // 返回带定位的父元素是什么 父级都没有定位返回body
元素.offsetTop         // 返回元素离带定位的父元素的上方有多远
元素.offsetLeft        // 返回元素相对于带定位的父元素左边框的偏移
元素.offsetWidth       // 返回自身包括padding+border+内容区 的宽度,不带单位
元素.offsetHeight      // 返回自身包括padding+border+内容区 的高度,不带单位

元素可视区client
常用属性:
元素.clientTop         // 返回元素上边框大小
元素.clientLeft        // 返回元素左边框大小
元素.clientWidth       // 返回自身padding+内容的宽度,不包含border,不带单位,不包括超出元素的内容
元素.clientHeight      // 返回自身padding+内容的高度,不包含border,不带单位,不包括超出元素的内容

元素滚动scroll
常用属性:
元素.scrollTop         // 返回元素被卷去的top距离,不带单位
元素.scrollLeft        // 返回元素被卷去的left距离,不带单位
元素.scrollWidth       // 返回自身padding+内容的宽度,不包含border,不带单位,包括超出元素的内容
元素.scrollHeight      // 返回自身padding+内容的高度,不包含border,不带单位,包括超出元素的内容
window.pageYOffset     // 返回页面被卷去的Y轴有多少
window.pageXOffset     // 返回页面被卷去的X轴有多少
例子:
document.addEventListener('scroll' , function(){
    console.log(window.pageYOffset);
})
```

### 动画函数

```
封装简单动画函数(需要给元素添加定位才能生效):
function animate(obj, target, callback) {
    clearInterval(obj.dingshiqi);
    obj.dingshiqi = setInterval(function() {
        var step = (target - obj.offsetLeft) / 10;
        step = step > 0 ? Math.ceil(step) : Math.floor(step);
        if (obj.offsetLeft == target) {
            clearInterval(obj.dingshiqi);
            if (callback) {
                callback();
            }
        }
        obj.style.left = obj.offsetLeft + step + 'px';
    }, 15);
}

缓动动画步长公式:
var step = (target - obj.offsetLeft) / 10;
step = step > 0 ? Math.ceil(step) : Math.floor(step);
回调函数动画:
调用时加上第三个函数,在函数当中去写需求
```

### 返回顶部功能

```
滚动窗口到文档中的指定位置
window.scroll(x,y)       // 滚动窗口到页面中的x,y位置,不要单位
```

# 移动端事件

```
触屏事件:
touchstart            // 手指触摸到dom元素时触发
touchmove             // 手指在dom元素上移动时触发
touchend              // 手指从dom元素移开时触发
触摸事件对象:
touches                // 正在触摸屏幕的所有手指列表
targetTouches          // 常用 正在触摸当前dom元素的所有手指列表
changedTouches         // 手指状态改变时触发
```
