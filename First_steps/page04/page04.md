## 变量

### 一、变量是什么

1. 变量不是存储的数据本身，更贴切的说，变量就是一个用于存放任意东西的 容器 ，容器中可以存放数字、字符串甚至其他更复杂的数据，如函数等
2. 顾名思义，存在变量中的值是可以改变的
3. 例子:[demo01](https://github.com/DeLei33534/JavaScript_Learning_Review/blob/master/First_steps/page04/demo01.html)

### 二、变量的声明

1. 使用变量的第一步是创建变量，即变量声明
2. 语法: let/var 变量名
3. 声明变量但是没有赋值，打印输出会得到一个 undefined 的返回值；使用一个从未声明的变量，则会报错
4. 为了避免不必要的麻烦，需要在变量声明后，对变量进行 初始化

   1. 变量的初始化，就是第一次为变量赋值的过程
   2. 可以在变量声明后，对变量进行赋值

      ```
        let name;
        name = "delei";

        /*
            在JavaScript中
            所有代码指令都会以分号结尾 (;)
            如果忘记加分号,单行代码可能执行正常
            但是在多行代码在一起的时候可能会出错
        */
      ```

   3. 也可以在声明变量的同时，对变量进行赋值
      ```
        let name = "delei";
      ```

### 三、var 与 let 的区别

1. 最初的 JS 中只有 var 关键字, 现代创建的 let 关键字是为了弥补，var 在一些开发场景中的不足
2. var 关键字

   1. 变量提升(var hoisting)

      1. 使用 var 声明的变量，总是会被放在任意代码开始执行前优先处理，这种行为叫做提升(hoisting)
      2. hoisting 就像是把所有的 var 变量声明，移动到函数或者全局代码的开头位置

      ```
       value = 2;
       var value;

       //可以隐式(implicitly)理解为

       var value;
       value = 2;
      ```

      3. 变量提升只会影响变量声明，而不会影响其值的初始化，只有执行到赋值语句时，变量才会被初始化

      ```
       /*
           //例一
           function todo(){
               console.log(value);
               var value = 123;
               console.log(value);
           }

           //可以隐式(implicitly)理解为

           function todo(){
               var value;
               console.log(value);
               value = 123;
               console.log(value);
           }
       */

       /*
          //例二，输出结果为undefinedA
          var x = y, y = 'A';
          console.log(x + y);

          //可以隐式(implicitly)理解为

          var x;
          var y;
          x = y;
          y = 'A';
          console.log(x + y);
       */
      ```

   2. 用 var 声明的变量，作用域是它当前的执行上下文
      1. 当前所在函数
      2. 对于声明在函数外的变量，为全局
   3. 变量可重新声明(相同变量名)
   4. 当给未声明的变量进行赋值时, 该变量会被隐式地创建为全局变量，将成为全局对象的一个属性
      1. 声明变量的作用域限制在其声明位置的上下文中，而非声明变量总是全局的
      2. 声明变量在任何代码执行前创建，而非声明变量只有在执行赋值操作的时候才会被创建

3. let 关键字
   1. 123123
4. 使用 var/let 声明变量的区别
   1. 对于一个多行的 JS 程序，可以在初始化一个变量后，再用 var 进行声明，程序仍可正常工作([demo02](https://github.com/DeLei33534/JavaScript_Learning_Review/blob/master/First_steps/page04/demo02.html))
   2. let 不支持上述做法，增强了代码的逻辑性与严谨性
   3. 使用 var 时，可以根据需要多次相同名称的变量(相当于变更变量值)，如
   ```
   var myName = "delei";
   var myName = "chfeng";
   ```
   1. let 同样不支持上述做法
