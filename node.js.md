# 模块开发规范

```
每一个js文件都是一个模块,内部定义的变量与函数在外部无法得到

如果需要模块之间相互使用,使用exports对象导出,require方法导入到其他模块

举例:
a.js中
let a = 1;
const b = b1 => console.log('123');
exports.属性名1 = a;
exports.属性名2 = b;

b.js中
let a = require('a.js的路径')
console.log(a.属性名1)
console.log(a.属性名2)

还可以使用module.exports进行导出
```
