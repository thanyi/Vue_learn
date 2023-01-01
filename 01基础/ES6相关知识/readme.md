# ES6 相关知识

## 箭头函数

箭头函数是一个es6中的一个函数简写方式，写的代码形式如下：
```javascript
var param  = function(){
    return "hello world";
}     //旧式写法

var param  = () => "hello world! ";     //新式说法

var param  = (a,b ) => {id:a,name:b};  



```
其中，箭头函数的相较于之前的表达方式：
- 省略了return和函数名
- 括号表示function函数的参数列表，注意的是，当函数代码不止一行时，需要用`{}`包裹函数代码
- 注意的

