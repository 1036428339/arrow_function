# 箭头函数

## 怎么用箭头函数

只有一个参数时，省略()
只有一条语句的时候 可以省略{} return

## 注意

参数箭头之间不能换行
返回一个对象的时候

## arguments

- 所有函数里面(除了箭头函数)都可以用的变量
- [arg1,arg2,gra3]

## 区别

- 箭头函数不支持重复命名形参，普通函数可以
- 箭头函数不能使用 call apply 等方法改变 this
- 箭头函数没有 this 它的this 指向定义时所处的上下文(外部函数)的this
- 箭头函数没有原型对象 .prototype
- 箭头函数不能作为构造函数(new 不出来)
- 箭头函数没有 arguments

## new target

- es6 引进的 返回 new 作用的那个函数(构造函数之中)

## 在使用 new 操作符来调用一个构造函数的时候，发生了什么呢？

- var person = new Person();可以分解为如下操作
- var obj  ={}; 创建一个空对象obj
- obj.__proto__ = Person.prototype; 将这个空对象的__proto__成员指向了构造函数对象的prototype成员对象，这是最关键的一步
- Person.call(obj); 将构造函数的作用域赋给新对象，因此call函数中的this指向新对象obj，然后再调用Person函数，给obj对象赋值
- return obj; 返回新对象obj

## 真正意义上的构造函数，需要满足下列条件

- 在函数内部对新对象（this）的属性进行设置，通常是添加属性和方法。
- 构造函数可以包含返回语句（不推荐），但返回值必须是this，或者其它非对象类型的值

## this 指针

- 与函数的运行方式有关

> 作为事件处理函数，this 指向事件发生的对象
> 是箭头函数 this 指向父级的this
> 普通函数 this 指向全局window(前端) global(后端)
> 作为对象的方法被执行，this 指向对象

## JS 数据类型

- 基础类型：数值型，字符串，布尔值，undefined，null，Symbol
- 复杂数据类型：Object (数组 对象字面量 函数)
- typeof 不能区分 找个工具 call
  Object.prototype.toString.call(varible);
  [object Array]

## classList

- contains add toggle

1. this.classList.add(first);//添加
2. this.classList.toggle(first);//有减无增
3. this.classList.contains(first)//是否包含
