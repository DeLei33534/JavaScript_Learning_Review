# 代码错误的解决

## 一、语法错误
1. 从控制台获取错误提示
   1. 红色三角代表抛出一个错误
   2. 查看错误信息
   3. 查看报错文件文件名
   4. 查看报错行
2. 检查对应文件相应位置代码

## 二、逻辑错误
1. 测试代码，观察异常行为(不符合预期的结果)
2. 检查对应逻辑代码块
3. 使用调试语句，如"console.log"观察打印结果
4. 订正业务逻辑

## 三、其它错误类型
1. SyntaxError: missing ; before statement(语法错误：语句缺少分号)
2. SyntaxError: missing ) after argument list(语法错误：参数表末尾缺少括号)
3. SyntaxError: missing : after property id(语法错误：属性ID后缺少冒号)
4. SystaxError: missing } after function body(语法错误：函数体末尾缺少花括号)
5. SyntaxError: expected expression, got 'string'(语法错误：得到一个 'string' 而非表达式)
6. SyntaxError: unterminated string literal(语法错误：字符串字面量未正常结束)
7. 等等......

## 四、JavaScript 常见错误参考
* https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Errors