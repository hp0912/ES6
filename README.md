# ES6

###### let 和 const 命令
1. let和const为ES6新增了块级作用域
2. let和const不存在变量提升，且存在暂时性死区
3. let不允许重复声明
4. const声明的变量不得改变值，const一旦声明变量，就必须立即初始化
5. ES6声明变量的6种方法：var function let const class import
6. let命令、const命令、class命令声明的全局变量，不属于顶层对象的属性

###### 变量的解构赋值
1. 常见的模式匹配
```
let [foo, [[bar], baz]] = [1, [[2], 3]];
foo // 1
bar // 2
baz // 3

let [ , , third] = ["foo", "bar", "baz"];
third // "baz"

let [x, , y] = [1, 2, 3];
x // 1
y // 3

let [head, ...tail] = [1, 2, 3, 4];
head // 1
tail // [2, 3, 4]

let [x, y, ...z] = ['a'];
x // "a"
y // undefined
z // []

const node = {
  loc: {
    start: {
      line: 1,
      column: 5
    }
  }
};

let { loc, loc: { start }, loc: { start: { line }} } = node;
line // 1
loc  // Object {start: Object}
start // Object {line: 1, column: 5}
```
2. 用途
  * 交换变量的值
  * 从函数返回多个值
  * 函数参数的定义
  * 提取JSON数据
  * 函数参数的默认值
  * 遍历Map结构
  * 输入模块的指定方法

###### 字符串的扩展

1. 字符的 Unicode 表示法
2. codePointAt()
3. String.fromCodePoint()
4. 字符串的遍历器接口
5. normalize()
6. includes(), startsWith(), endsWith()
7. repeat()
8. padStart()，padEnd()
9. matchAll()
10. 模板字符串
