# Vue中的数据代理

## 关于Object.defineProperty()方法

这是一个在js中可以在代码中设置属性的方法，有点像是java中的反射（但是我java学的不好可能有点点出入）

```javascript
let number = 18
let person = { name:"ethanyi", 
                sex:"male",
               }  
               
Object.defineProperty(person,'age',{
                //value:18,       //这个可以直接设置或者是使用set方法
                
                
                //有很多其他的相关配置可以作为对象参数进行传输
                enumerable:true,    //控制这个属性可不可以被枚举
                writable:true       //控制这个属性可不可以被修改
                
                get(){
                return number ;
                }
                set(value){
                number = value；
                }
```

这里其实最重要的就是`get()`和`set()`方法，我感觉它是一个框架可以进行实施的，最重要的两个方法，现在来说就是作用是更改和获取对象中的参数的值。
