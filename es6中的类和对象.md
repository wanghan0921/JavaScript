### 1.es6中的类和对象

1. 类是抽象的, 对象是具体的

  例如: 手机是一个类, 可以泛指各种手机苹果, 华为, oppo等等, 对象就是具体的 , 通过对类的实例化, 创建出苹果手机对象, 华为手机对象等等
  
  
### 2.对象

万物皆对象, 对象一定是一个具体事物.

在JavaScript中, 对象是一组无序的相关属性和方法的集合 所有的事物都是对象, 例如字符串, 数组, 数值, 函数等

对象是由属性和方法组成的: 

+ 属性: 事物的特征, 在对象中用属性来表示
```js
string.length
```

+ 方法: 事物的行为, 在对象中用方法来表示
```js
string.substring(1)
```

### 3.类

在es6中,可以用class关键字声明类

#### 3.1 创建类

```js
class Person {
  // 这个函数可以接受传递过来的参数, 同时返回实例对象
  // 就算没有定义, 只要new的时候也会自动生成
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  des() {
    return this.name + '的年龄是' + this.age
  }
}

let xiaoming = new Person('xiaoming', 18)
xiaoming.des()
```

> 补充: new关键字都做了什么?
>  1. 创建一个新对象
>  2. 将新对象的_proto_指向构造函数的prototype对象
>  3. 将构造函数的作用域赋值给新对象 （也就是this指向新对象）
>  4. 执行构造函数中的代码（为这个新对象添加属性）
>  5. 返回新的对象

```js
var Obj = {};
Obj._proto_ =  Person.prototype();
Person.call(Obj);
```


























