# 2020 年 8 月 7 日

> 笔记一：

### 标题

```
<h1>一级标题</h1>
<h2>二级标题</h2>
<h3>三级标题</h3>
```

### 分割线

```
<hr>
```

### 段落

```
<p>段落</p>
```

### 表格

```
<table>表格（border）线框效果</table>
<caption>标题</caption>   // table中的标题
<tr>行 </tr>
<th>表头标签</th>--加粗居中
<td>列，单元格</td>
<thead>头部区域</thead>
<tbody>主体区域</tbody>
<tfoot>底部区域</tfoot>
rowspan="合并个数"--跨行合并
colspan="合并个数"--跨列合并
```

### 超链接

```
<a href=""> </a>
href--链接地址
href中输入javascript:; 阻止连接跳转
target="_blank" 或 ="self"--链接打开方式
title--信息提示
压缩包或文件会直接下载
```

### 锚点连接

```
<a href="#名字"> </a>
找到需要跳转的位置添加id名字
<位置 id="名字"> </位置>
```

### 配置设置

```
<meta charset="utf-8">---设置允许支持中文格式
```

### 图片插入

```
<img src=""  alt="">
src--图片地址
alt--图片找不到时的提示信息
title--信息提示
```

### 表单

```
<form action="url地址" method="提交方式(post有安全性/get无安全性)" name="表单域名称">--表单域
<input type="text" name="">   // name中输入名称
<input type="submit" value="">--提交按钮，发送给服务器,value输入按钮名称
</form>

下拉表单:
<select>--至少包含两个
 <option>内容</option>
 <option selected="selected">内容</option>--网页出现时的首选内容
</select>

文本域表单:
<textarea cols="" rows="">
内容               // cols文本域内可见宽度 rows文本域内可见行数
</textarea>


```

### 输入框 常与表单一起用

```
<input type="text">--任意内容
<input type="search">--搜索框
<input type="time">--时间文本框
<input type="date">--日期文本框  常用
<input type="month">--月文本框
<input type="week">--星期文本框
<input type="tel">--手机号码
<input type="color">--颜色选择表单
<input type="url">--限制用户输入必须为url类型
<input type="email">--限制用户输入必须为email类型 必须添加在form表单域中
<input type="number">--数字
<input type="password">--内容不可见,密码框
<input type="radio">--单选按钮（当实现多选一时 需要在表单的name设置同一个名字）
<input type="checkbox">--复选框，可以只有一个
（当实现多选时，需要在表单的name设置同一个名字）
<input type="submit">--提交按钮，发送给服务器
<input type="reset">--重置按钮，重置表单中所有数据
<input type="button">--普通按钮（与js搭配）
<input type="file">--定义输入字段和“浏览”按钮，供文件上传
<input type="file" multiple>--多个文件上传
<input type="hidden">--隐藏输入字段
<input type="image">--图像形式的提交按钮
<input name="名称">--input中的名称
<input value="值">--input中的值
<input checked="checked">--input中首次加载会被选中
<input maxlength="正整数">--input输入的字符最大长度
<input type="" placeholder="提示内容">--输入框中提示用户输入的内容

h5新增属性:
required="required"        // 必填内容
placeholder="提示信息"      // 表单提示信息,需要提示什么就输什么
autofocus="autofocus"      // 自动获得焦点
autocomplete="off/on"      // 提示以前用户成功输入并提交的内容,需要加上name属性
multiple="multiple"        // 多选文件提交
```

### label(常与表单一起用)

```
<label>
<input type="radio" name=" " id="名字" />
</label>--包裹住所有内容以扩大选定范围
```

### 盒子模型

```
<div></div>--盒子/容器
行内元素[span]--对宽高设置无效，宽高根据内容来定
块级元素[div]--独占一行，可设置宽高
```

### 列表

```
<ul>--无序列表
<li></li>
</ul>
list-style: none;

<ol>--有序列表
<li></li>
</ol>

<dl>--自定义列表
<dt></dt>--标题
<dd></dd>--内容
</dl>

list-style:none--取消基本样式
```

### 注释

```
ctrl+/--注释文字
```

### 字符实体,特殊字符

```
&nbsp;--空格
&lt;--小于
&gt;--大于
&amp;--和号    显示效果&
&quot;--双引号
&apos;--单引号  ie不支持
&yen;--人民币
&copy;--版权
&reg;--注册商
&deg;--摄氏度
&plusmn;--正
&times;--乘号
&divide;--除
&sup2;--上标2
&sup3;--上标3
```

### html5 新语义标签 (手机端使用)

```
<header></header>        // 网页头部
<nav></nav>              // 网页导航
<footer></footer>        // 网页底部
<aside></aside>          // 网页侧边栏
<section></section>      // 网页区块
<article></article>      // 网页文章
```

### 视频与音频

```
<audio src=""></audio>  // 音频标签支持MP3 Wav Ogg 尽量使用MP3
属性:
autoplay="autoplay"     // 自动播放
controls="controls"     // 显示播放控件
src="url"
loop="loop"             // 循环播放

<video src="" controls="controls"></video>  // 视频标签 尽量使用MP4格式
属性:
autoplay="autoplay"     // 自动播放 谷歌浏览器需要添加muted才有效
muted="muted"           // 静音
controls="controls"     // 显示播放控件
width=" px"             // 宽度
height=" px"            // 高度
loop="loop"             // 循环播放
preload="auto/none"     // 预加载 none为禁止,有autoplay则忽略本条
src="url"
poster="url"            // 加载等待时的图片
```

# HTML 认知

```
初始设置
<!DOCTYPE html>
// doctype是文档类型声明,声明该网页的HTML版本 上述为html5
<html lang="en">
// 标识网页使用的语言 zh-CN简体中文 en英文 可以用作搜索引擎归类和浏览器翻译
<head>
    <meta charset="UTF-8">
    // 标识网页的字符编码 UTF-8是万国码
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    // 解决ie浏览器兼容性
    <meta name="viewport" content="width=device-width,
    initial-scale=1.0">
    // 宽度与设备宽度相等,移动端网页使用
    <title>Document</title>
</head>


SEO:
搜索引擎优化,使得网站在搜索引擎中排名靠前
提升排名的方法
1.竞价排名
2.将网页制作为html后缀
3.标签语义化 在合适的地方用合适的标签
等等
SEO三大标签
title            // 网页标题标签
description      // 网页描述标签 在标题上方meta使用 meta:desc
keywords         // 网页关键词标签 在标题上方meta使用 meta:kw


标题图标
<link rel="stylesheet" href="ico图标路径" type="image/x-icon">
改ico图标的路径,图片格式是ico
```
