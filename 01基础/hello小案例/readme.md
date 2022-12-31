# Vue会话

## 写在前面
vue的特点是什么？
- vue主要是可以实现**组件化**的前端控制，在进行前端设计的时候，一个.vue文件就是一个特别的包含了js三件套的组件，这极大的方便了我们进行前端如此多模块的构建。
- vue是一个**声明式**的编码流程，也就是我们不需要一点一点命令这些代码做什么，而是我们直接写好一个框架了之后vue框架自己就可以对其进行识别

## 第一个例子
所有的语言的第一个例子就是helloworld，我们来进行一下
```html
<body>
    <div id="root">
       <h1>{{name}}</h1> 
    </div>


    <script src="https://cdn.jsdelivr.net/npm/vue@2.7.14/dist/vue.js"></script>
    <script>
        new Vue({
            el:'#root',
            data:{
                name:'helloworld',
            }
        })
    </script>
</body>
```

这里我们可以知晓，其中 `new Vue()`是用来进行vue对象创建的，整个vue的使用都离不开这个对象，其中`el`属性是用来和div标签进行一一绑定的。

这份绑定只能是一对一，当有一个div和两个相同的vue对象进行绑定的时候，此div标签只会和第一个vue对象进行绑定，后面的无论有多少对象都不会进行绑定。
同理，如果有多对一，多个div绑定了一个vue对象，那么就只有第一个div容器是可以和vue对象形成对应关系的，后面的div容器都无法和vue对象进行联系。

以上代码结果如下：
![image](https://user-images.githubusercontent.com/68628311/210136612-f4961589-9a78-48be-b98f-625d37f58a43.png)
