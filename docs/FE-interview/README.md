---
sidebar: auto
---

# 前端面试题

## HTML

## CSS

### 层叠上下文



## Javascript

### 原型和原型链

1. 构建**函数**的 prototype->函数创建的**实例**的原型->实例的`__proto__`
2. 原型对象的 `constructor` 属性->构造函数本身
3. `Person.prototype === person1.__proto__`
4. 特点
   - 原型对象上添加属性，实例会共享这些属性
   - 在对象查找自身没有的属性时，会从对象的原型上找，找不到就找原型的原型，一直找到 Object.prototype，还找不到返回 null
5. 原型链就是查找对象查找属性时所途径的链式结构。

### 作用域和作用域链

1. 作用域：代码**定义变量**的区**域**。有一套**规则**，规定了**如何查找**变量，确定当前执行代码对变量的**访问权限**。
2. 分类：全局、函数和 eval 作用域。
3. 特点：JS 是**静态作用域**，函数的作用域在函数创建的时候就已确定。
4. 规则：作用域可**嵌套**，在查找变量时，先从当前作用域中查找，找不到就在外层的作用域中找，直至全局作用域，然后停止查找。
5. 作用域链：**逐层嵌套**的作用域构成的链表结构就是作用域链。

### 闭包

1.  怎么产生闭包
    - 函数嵌套，内函数引用了外函数的变量
2.  什么是闭包
    - 两种理解。
    - 内函数。
    - 包含引用变量的对象，chrome debugger scope 中的 closure。
3.  闭包的作用
    - 延长生命
    - 外部可用(突破作用域)
4.  闭包的缺点
    - 变量未释放->占内存
    - 滥用->内存泄漏

### this 的指向

1. 默认情况，非严格模式，this 指向全局对象
2. 在函数中 this 一般指向调用该函数的对象
3. 使用 call,apply,bind 方法可显式指定 this 的指向
4. 使用 new 调用构造函数，函数中的 this 指向新创建的实例对象
5. 箭头函数没有自己的 this，函数中的 this 指向箭头函数所在的上下文中的 this

### js 执行机制

### js 中有哪些类型

答：8 种，undefined、null、number、string、boolean、symbol、bigInt、object。

### null 与 undefined 的区别

- undefined 表示变量声明了**未赋值**。
- null 赋值了，值为空，表示变量未来可能指向一个对象，可用于**主动释放** 对象的引用。

### == 和 === 的区别

- === 判断类型和值是否相同，对象比较的是地址值。
- == 类型相同，同===，不同会做隐式类型转换，具体判断流程如下：
  - 判断类型，相同则使用===，不相同，做类型转换
  - 判断是否对比 null 和 undefined，是就返回 true
  - 判断是否对比 string 和 number，是就将 string 转成 number 再比较
  - 判断其中一方是否为 boolean，是就将 boolean 转成 number 再比较
  - 判断其中一方是否为 object，且另一方为 string，number，symbol，是就把 object 转成原始类型。

### 类型转换原理

### 为什么会有bigint提案

### 为什么0.1+0.2!=0.3

### 类型判断

### 变量提升和函数提升

### ES6模块与CommonJS模块的区别

### V8 垃圾回收机制

### 事件循环

- js 中有一个主线程和一个调用栈，和独立于调用栈的宏任务队列和微任务队列
- 宏任务：script 代码，setTimeout/setInterval/setImmediate, I/O, UI rendering
- 微任务：process.nextTick, Promise, Object.observe, MutationObserver
- 代码执行过程中，将任务的各自回调函数根据任务类型放入对应的任务队列中
- 主执行栈清空，执行微任务队列，微任务清空，再执行宏任务中的一个任务

### JS异步方式

- 回调函数
- promise
- generator
- async/await

## Vue相关

### 虚拟DOM

### diff原理

### MVVM原理

### 怎么实现vue的minin方法

### Vuex的原理

### Vue-Router的原理





## 手写与算法

### 实现类的继承

### 实现new

### 实现Object.create

### 实现instanceOf

### 实现call、apply和bind

### 实现防抖节流

### 实现deepClone

### 实现Promise

### 实现事件订阅发布

### 



### 排序算法



## 浏览器、HTTP和前端安全

### 浏览器渲染过程

### load、DOMContentLoaded事件的触发顺序



### WEBSOCKET握手过程

### 前端安全问题



## 前端工程化和优化

### 首屏优化