# JavaScript学习笔记



## 一、认识JS

JavaScript是一种轻量型、解释型、面向对象的脚本语言。它主要被用于在网页上实现动态效果，增加用户与网页的交互性。作为一种客户端脚本语言，JavaScript可以直接嵌入HTML，并在浏览器中执行，使得网页不再是静态的，而是可以根据用户的操作动态变化的。

JavaScript的作用：

- 客户端脚本：用于在客户浏览器执行，实现动态效果和用户交互。
- 网页开发：与HTML和css协同工作，使得网页具有更强的交互性和动态性
- 后端开发：可以在服务器端进行，实现服务器端应用的开发

## 二、导入方式

- 内联导入：

在head标签或者body标签创建一个script标签

```
 <script>
       console.log('hello,body的内联样式');
 
 </script>
```

显示在浏览器F12控制台

- 外联导入

创建一个js文件

```
 <script src="./js/myscript"></script>
```

## 三、基本语法

1) 数据类型

3个关键字定义变量：

- var：声明一个正常的变量 var x;
- let:    let y=5;
- const:  声明一个常量 const pi=3.14

var和let都是变量，var声明的变量具有函数作用域，let具有块级作用域更安全更灵活

```
<script>
var x;
let y=5;
const pi=3.14;
console.log(x,y,z);
let name='如花';
console.log(name);


<script>
```

2. 控制语句

   1）条件语句

   ```
   if(condition)
   {
   如果条件为真，执行这里的代码
   }
   else if(condition2)
   {
   条件2为真，执行这里的代码
   }
   else
   {
   如果为假，执行这里的代码
   }
   ```

   2）循环语句

   ```
   for(循环初始表达式；循环条件；迭代器)
   {
   循环体，执行这里的代码
   }
   
   for(let i=1;i<=10;i++)
   {
   console.log(i);
   }
   ```

   ```
   while(循环条件)
   {
   循环体，执行这里的代码
   }
   
   let count=1
   while(count<=10)
   {
   console.log(count);
   count++;
   }
   ```

   ## 四、函数、事件、DOM