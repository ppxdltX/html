# URL 统一资源定位符

```
三部分组成:
https://lol.qq.com/main.shtml 举例
1.客户端与服务器之间的通信协议  https
2.存有该资源的服务器名称  lol.qq.com
3.在服务器上的具体位置  main.shtml
```

# HTTP 协议

```
超文本传输协议,规定了浏览器与服务器之间通信的规则
```

# 客户端与服务器的通信过程

```
过程分为三个步骤:
1.请求---客户端发起请求
2.处理---服务器处理请求
3.响应---服务器响应客户端

两个请求方式
get 向服务器获取数据
post 向服务器提交数据
```

# XML 可扩展标记语言,不使用了,现在用 JSON

```
被设计用来保存和储存数据的
所有标签都是自定义标签,没有预定义的标签
<zdy1></zdy1>
<zdy2></zdy2>
<zdy3></zdy3>
```

# JSON

```

```

# jQuery 中的 ajax

```
jQuery
$(function(){
    $('对象名称').on('事件', function(){
        get('url')
    })
})

$.get('url',[data],[callback]) // 专门发起get请求,url是请求的资源地址,中括号代表可选请求,data是请求资源期间要携带的参数需要以对象的形式,callback是请求成功时的回调函数

$.post()

$.ajax()
```

# express 框架

```
1.引入express:
const express = require('express');

2.创建应用对象
const app = express();

3.创建路由规则
app.get('/', (request, response)=>{})  // request是请求报文的封装  response是响应报文的封装

4.监听端口启动服务
app.listen(8000, ()=>{
    console.log(111);
})
```
