# JavaScript 的组成
JavaScript 基础分为三个部分：

- ECMAScript：JavaScript 的语法标准。包括变量、表达式、运算符、函数、if 语句、for 语句等。

- DOM：文档对象模型，操作网页上的元素的 API。比如让盒子移动、变色、轮播图等。

- BOM：浏览器对象模型，操作浏览器部分功能的 API。比如让浏览器自动滚动。
### JavaScript的数据类型
1. 基本（原始）数据类型
    - 数字  number
    - 字符串 string
    - 布尔数值 boolean
    - 未定义  undefined
    - 空值   null      
2. 引用（复杂）数据类型
    - object类型     
    - array类型      数组
    - function函数

### 变量和常量（字面量）
1. 常量：即常量，是固定值，不可改变。看见什么，它就是什么。
- 分为数字或者字符串
    - 数字不需要加什么符号，直接写上即可。数分为整数和浮点数（小数）
    - 字符串需要加上引号，单引号和双引号都可以。_**单引号不能嵌套单引号，双引号也是，但可以单引号嵌套双引号，双引号嵌套单引号。**_
2. 变量：变量可以用来保存字面量，而且变量的值可以任意改变。可以理解为变量是储存数据的容器
- 变量名有命名规范：__只能由英语字母、数字、下划线、美元符号$构成，且不能以数字开头，并且不能是 JavaScript 保留字。__
    - var 是英语“variant”变量的缩写。后面要加一个空格，空格后面的东西就是“变量名”：

    - 定义变量：var 就是一个关键字，用来定义变量。所谓关键字，就是有特殊功能的小词语。关键字后面一定要有空格隔开。

    - 变量的赋值：等号表示赋值，将等号右边的值，赋给左边的变量。

    - 变量名：我们可以给变量任意的取名字。
### 我们来整理一下变量的命名规则：

1.变量命名必须以字母或是下标符号”_”或者”$”为开头。

2.不能以数字开头

3.不能是 js 中的关键字和保留字

4.严格区分大小写

5.建议用驼峰命名规则：getElementById/matherAndFather/aaaOrBbbAndCcc

6.见名知意
## 转义字符
在字符串中我们可以使用\作为转义字符，当表示一些特殊符号时可以使用\进行转义。
例如:\\'表示',\\"表示"...

###### typeof 运算符
typeof()表示“获取变量的类型”，返回的是小写，语法为：typeof 变量

typeof 数值的返回结果：number

typeof 字符串的返回结果：string

typeof 布尔型的返回结果：boolean

typeof undefined的返回结果：undefined

$\color{red}{typeof null的返回结果：object}$

### 由于内存原因Number的表示问题
最大值：Number.MAX_VALUE，这个值为： 1.7976931348623157e+308

最小值：Number.MIN_VALUE，这个值为： 5e-324 （e表示的是以10为底数）（5乘以10的负324次方）

如果超过了以上的数值，则用Infinity表示正无穷大，-Infinity表示负无穷大。
### NaN 和 isNaN()函数：
NaN是一个特殊的数字，表示 Not a Number，非数值。

$\color{red}{注意：typeof NaN的返回结果是 number。}$

isNaN() :任何不能被转换为数值的值，都会让这个函数返回 true。

isNaN(NaN); // true
isNaN("blue"); // true
isNaN(123); // false

$\color{blue}{浮点数的运算：在 JS 中，整数的运算基本可以保证精确；但是小数的运
算，可能会得到一个不精确的结果。所以，千万不要使用 JS 进行对精确度要求比较高的运算。}$

我们知道，所有的运算都要转换成二进制去计算，然而，二进制是无法精确表示 1/10 的。因此存在小数的计算不精确的问题。
### Boolean 布尔值

true 和 fase。主要用来做逻辑判断。布尔值直接使用就可以了，千万不要加上引号。

代码：var a = true;
console.log(typeof a); 输出为boolean

变量值的传递："=" 赋值的意思 

# 变量的类型转换

##转成 字符串 
 方式一 :  调用 toString()方法...
1. 数字类型
var num = 123;
num = num.toString();
console.log(num); // 123
var num2 = 345;
console.log(num2.toString(2)); // 101011001
2. 布尔值
console.log(true.toString()); // true
3. null 和 undefined  没有 toString 方法
 console.log(null.toString())

方式二 : 使用String()
1.数字
    console.log(String(345)); // 345
2. 布尔值
    console.log(String(false)); //false
null 和 undefined 
console.log(String(undefined)); // undefined
console.log(String(null)); // null 

方式三  +'';  拼接作用
console.log(123);
console.log(123 + ''); // 123
console.log(true + '');
console.log(undefined + '');     引号之间没有任何空格
console.log(null + '');

$\color{green}{只有函数toString的undefined和null不能转换，其他都可以。}$


## 转成 数字类型
方式一 Number();
1 字符串
console.log(Number('123')); // 123
console.log(Number('abc123')); // NaN
console.log(Number('')); // 0
console.log(Number('     ')); //0 

$\color{green}{纯正数字的字符串可以转换为数字，有字母混杂的转换为NaN，空的双引号或者存在空格的转换为0}$

2  布尔值
console.log(Number(true)); // 1
console.log(Number(false)); // 0
3 undefined 和 null
console.log(Number(undefined)); // NaN
console.log(Number(null)); //0


## 转成布尔值 Boolean()
1  字符串
console.log(Boolean('')); // false
console.log(Boolean(' ')); // true 
console.log(Boolean('false')); // true
2. 数字
console.log(Boolean(0)); // false
console.log(Boolean(NaN)); // false
3 undefined 和 null
console.log(Boolean(undefined)); // false
console.log(Boolean(null)); // false

console.log(Boolean({})); // true
$\color{green}{总结: NaN 0 undefined  null  '' 这五种转换为false,其余 都是true}$



$\color{green}{强调 ,涉及到隐式转换 时   所使用的时  String()  Number()  Boolean()}$

### 算数运算符
加减乘除 取余  括号
1.  非数值进行加减乘除取余时,会先转换成  数字类型 (隐式转换) Number()
console.log(true + 1); // 2
console.log(null + 1); // 0+1=1
console.log(undefined + 1); // NaN
console.log('11' - 1); // 10
这个 +  号  拼接字符串的作用  加法(只要有一方是字符串,那就是拼接)
console.log('11' + 1); // 111
2. 任何值和 NaN 做运算的结果都是 NaN。
3. 任何的值和字符串做加法运算，都会先转换为字符串，然后再做拼串操作。
4. 任何值做-、*、/运算时都会自动转换为 Number。

### 自增自检
+= 和-=        
~~~        var n = 10;
        // 把 n+ 5 的 结果 赋给 n
        n = n + 5; // 15
        // 简写成
        n += 5; // 20
        console.log(n);
        n -= 10; // 10
~~~

### ++a  和  a++ 的区别
        相同 : 都实现了 a 往上 加1
        a=++a  是  先++再赋值  (返回的结果 是 +1 之后的值)
            可以写成  a++;然后再用a
            例如 temp=arr(++a);====>a++; temp=arr(a);
        a=a++  是 先赋值 后++  (返回的结果  是  +1  之前的值)

### 比较大小
        // >  <  >= <=  == !=   ===(严格相等)  !==
        // 比较运算符  通过 返回 true  或者 false  来表明比较的结果
        console.log(3 > 5); // false
        console.log(3 <= 5); // true


        // 非数值的比较 会将其转换为数字然后再比较。
        console.log(true > 0); //true
        console.log(10 < '100'); // true

        // 任何值和NaN做任何比较都是false
        console.log(10 > 'hello'); // false

        // 特殊  两边都是字符串 不会将其转换为数字进行比较。  而是比较unicode 编码
        console.log('123' > '59'); // false
        console.log('hello' > 'world'); // false 104  >119



        // 重点   ==  和 ===  区别
        console.log(5 == '5'); //true
        console.log(undefined == null); // true
        console.log(NaN == NaN); //false
        // 严格等于 先比较数据类型,再比较大小
        console.log(5 === '5'); // false
        console.log(undefined === null); //false


        // ==的反面是!=，===的反面是!==
        console.log(3 != 5); // true

### parseInt parseFloat
        // parseInt()  转换为整数
        // parseFloat()  转换为 小数
        // parseInt()的作用是将字符串中的有效的整数内容转为数字。parse 表示“转换”，Int 表示“整数”（
        var a = '12345';
        var b = '123.4';
        console.log(parseInt(a)); // 12345
        console.log(parseFloat(b)); // 123.4

        var c = '123a';
        console.log(parseInt(c)); // 123
        console.log(parseInt('    2019abc')); // 2019
        // 转换规则: 从第一个非空白字符（空格、换行、tab）开始转换，直到遇到一个非数字字符为止。
        // 不会四舍五入  取整
        var sum = parseInt(5.8) + parseInt(4.7); //
        console.log(sum); // 9  

        // 非字符串
        // 如果对非 String使用 parseInt()或 parseFloat()，它会先将其转换为 String然后再操作。


        // parseFloat()：字符串 --> 浮点数（小数）
        var d = "123.456.789px";
        console.log(parseFloat(d)); // 123.456