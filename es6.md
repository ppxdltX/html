# let

```
特点
1.变量不能重复声明
2.块级作用域
3.不存在变量提升
4.不影响作用域链
```

# const 定义常量

```
特点
1.一定要赋初始值
2.一般常量都大写(也能小写)
3.一般常量的值不能修改
4.块级作用域
5.对于数组与对象的值是可以修改的,因为指向的是地址
```

# 解构赋值

```
1.数组解构赋值
const a = ['1','2','3','4','5'];  // 创建数组
let ['一','二','三','四','五'] = a;  // 解构赋值

2.对象的解构赋值
const a = {
    name:'X';
    age:'18';
    sex:'man';
    zuoping: function(){
        console.log(111);
    }
}
let {name,age,sex,zuoping} = a;   // 一般调用
let {zuoping} = a;
zuoping();      // 不单独解构的话格式是a.zuoping{};较为复杂
```

# 新的声明字符串方式

```
es6以前有'' , "";
es6中新方法 ``;
新特性:
1.内容中可以直接回车换行
2.变量能够直接拼接在内容中,固定格式为 ${}
举例:
以前 let a = '3';
     let b = '还有' + a + '天';
现在 let a = '3';
     let b = `还有${a}天`;
```

# 简化对象写法

```
let a = '1';
let b = function(){
    console.log(2);
}                    // 声明两个变量

const obj = {
    a,
    b,                    // 简化对象内变量写法
    c(){
        console.log('3')  // 简化对象内函数写法
    }
}
```

# 箭头函数

```
let 变量 = (形参1,形参2) => {   //声明函数
    return 形参1 + 形参2;
}

let 名称 = 变量(实参1，实参2);  // 调用函数
console.log(名称);

特征
1.this是静态的,始终指向函数声明时作用域下的this的值 普通函数:谁调用我我指向谁 箭头函数:我在哪里创建的,我就指向谁
2.不能作为构造函数
3.不能使用arguments变量
4.箭头函数的两个简写:
let a = n =>{    // 当形参有且只有一个时,可以省略小括号
    return n + n;
}
console.log(a(1));

let a = n => n + n;  // 当函数内只有一条语句时,可以省略大括号,此时return也必须省略
console.log(a(2));

使用箭头函数返回偶数组
const arr = [1, 2, 3, 6, 5, 94, 35, 84, 651, 654]
const result = arr.filter(function(e) {
    if (e % 2 === 0) {
        return true;
    } else {
        return false;
    }
})
console.log(result);
简化为 const result = arr.filter(e => e % 2 === 0);

适用于与this无关的回调,定时器,数组的方法回调
```

# 函数参数赋值初始值

```
可以给函数形参赋初始值,如果没有传递实参则使用该初始值,否则使用实参
```

# rest 参数

```
代替arguments的获取函数实参的参数
用法:
function a (形参1,形参2,形参3,...名称){}   // 在前面加上三个点
```

# 扩展运算符

```
同样是[...] 能够将数组转化为参数序列
const a = [1,2,3,4,5];
function b(){
    console.log(arguments);
}
b(...a);    // ...加上数组可以转化为参数序列,用逗号分开

还能够合并数组:
const a = [1,2,3,4,5];
const b = [6,7,8,9,10];
const c = [...a,...b];  // 中间使用逗号隔开
console.log(c);

数组克隆:
const a = [1,2,3,4,5];
const b = [...a]; // 将a的内容克隆到b中,有引用类型的数据是浅拷贝
console.log(b);

将伪数组转为真正的数组:
const divs = document.querySelectorAll('div');
const divArr = [...divs];   // 这样能使用数组的方法
```

# Symbol 数据类型

```
特点
1.Symbol 的值是唯一的
2.Symbol 的值不能与其他数据进行数据运算,比较
3.Symbol 定义的对象属性不能用for...in循环遍历,只能使用Reflect.ownKeys来获取所有对象的键名

给对象添加独一无二的属性方法
 let a = {
     name: '1',
     sex: 'man'
 }
 let b = {
     h: Symbol
 }
 a[b.h] = function() {}
和
let a = {
     name: '1',
     sex: 'man'
     [Symbol('h')]: function(){}  // 括号内h是描述字符串
```
