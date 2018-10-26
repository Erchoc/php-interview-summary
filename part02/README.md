## part02. JavaScript, jQuery, Ajax 基础考察点

1. 下列不属于 JavaScript 语法关键/保留字的是()?
> A: var, B: $,C: function,D: while,

2. JavaScript 中为 id 是 test 的元素设置样式为good。
> document.getElementById('test').className = 'good';

3. 要求使用 jQuery 事件写在页面元素加载完成后, 动态绑定click事件到 btnOK 元素。
> $(function () {
>   $("btnOK").click(function () {
>     xxx 
>   });
> })

4. AJAX 技术利用了什么协议?请简述 AJAX 的工作机制。
> 

#### JavaScript 基本语法
- 变量定义: $ 或 _ 或字母开头, 大小写敏感, 使用 var 声明变量, 可使用逗号在一个语句种声明多个变量
- 注意: 生命不赋值变量，变量的值默认为undefined。如果重新声明变量不赋值，其值不会丢失。
- 数据类型: 字符串String, 数字Number, 布尔Boolean, 数组Array, 对象Object, Null, Undefined
- 注意: 所有数据类型变量均为对象, 创建对象方式有 new Object() , 使用 JSON 对象和使用对象构造器。

#### 函数
- 无函数默认值说法, 函数内部声明的变量是局部变量, 外部无法访问; 函数内部声明的变量是全局变量, 所有脚本和函数都能访问。
- 运算符: 拼接字符串使用 + 号。
- 流程控制: else if 必须分开写，PHP中可以选择合起来写。

#### JavaScript 内置对象
- Number
```
var pi1 = 3.14;
var pi2 = Number(3.14);
var pi3 = new Number(3.14);
```
- String
```
var str1 = 'This is a String';
var str2 = String('This is a String');
var str3 = new String('This is a String');
```
- Boolean
```
var bol1 = true;
var bol2 = Boolean(true);
var bol3 = new Boolean(true);
```
- Array: 没有关联数组
```
var arr1 = new Array();
var arr2 = new Array(3);
var arr3 = new Array(e1, e2, e3);
```
- Date
```
var date = new Date();
```
- Math
```
var pi = Math.PI;
var sqrt = Math.sqrt(15);
```
- RegExp: 正则表达式对象不要使用引号
```
/pattern/attributes
new RegExp(pattern, attributes);
```
- Window对象
```
Window
Navigator
Screen
History
Location
```
- DOM对象
```
Document
Element
Attr
Event
```
#### jQuery基础知识
- jQuery 选择器
```
基本选择器
层次选择器
过滤选择器
可见性过滤选择器
属性过滤选择器
子元素过滤选择器
表单对象过滤选择器
```
- jQuery 事件操作
```
$("button").click(function() {

});
```
- jQuery 效果
```
$("p").show();
```
- jQuery DOM 操作
```
属性
值
节点
样式
尺寸
```
#### Ajax 基础考察点
- 工作原理: 基于 XMLHttpRequest 对象, 与后台服务器交换数据
```
open(method, url, async);
send(string);

responseText();
responseXML();

onreadystatechange();
readyState: 0(请求未初始化), 1(服务器连接已建立), 2(请求已接收), 3(请求处理中), 4(请求已完成且响应已就绪)
status: 200, 404;
```

- JavaScript

- jQuery
```
$(ele).load();
$.ajax();
$.get();
$.post();
$.getJSON();
$.getScript();
```
- Vue

- React

#### 解题方法
> JavaScript 的 HTML 样式操作和 jQuery 的选择器, 事件和样式操作。

