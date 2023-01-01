# ES6 相关知识

  ## 箭头函数

  箭头函数是一个es6中的一个函数简写方式，写的代码形式如下：

  ```javascript
  var param  = function(){
      return "hello world";
  }     //旧式写法
  
  var param  = () => "hello world! ";     //新式说法
  
  var param  = (a,b) => {id:a,name:b};  
  
  ```

  其中，箭头函数的相较于之前的表达方式：

-  省略了return和函数名

-  括号表示function函数的参数列表，注意的是，当函数代码不止一行时，需要用`{}`包裹函数代码


  ## 代码简化

  es6中有很多关于代码简化的地方，这里挑选几个我存在印象的记录一下

  

  ### 对象简化

  ```javascript
   //es6之前的写法
  const people = { name:"name", 
                  age:"age",
                  grade: function(){
                      return 100;
                  }   
                 }  
                              
   //es6之后的写法                            
  const people = { name, 
                  age,
                  grade(){
                      return 100;
                  }   
                 }  
  ```
  也就是说，对于es6来说，

- 当对象中的key和value是一样的字符串，那么在对象之中可以直接写成一个参数，代表值和键是一模一样的
- 对象中的函数可以进行合并，变成`函数名(){函数代码}`的形式
                  
