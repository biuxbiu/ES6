# ES6

## 什么是ES6

`ES6` 是下一代 `Javascript` 的语言标准，已经在 2015年6月发布，目前我们很多框架很应用都已经在使用 `ES6` 了。



## let和const

`ES6` 中新增了 `let` 和 `const` 。它们的作用和 `var` 差不多，但是有一些小区别。

* let

`let` 声明的变量只在该代码块内有效。

```javascript
{
    let x = 1;
    var y = 2;
}

//x is not defined
//y 2
```

<br>

在 `for` 循环里面，就很使用 `let` 。

```javascript
for (let i = 0; i < 5; i++){
    console.log(i);         //0 1 2 3 4
}
```

```javascript
for (let i = 0; i <5; i++){
}
console.log(i);             // i is not defined
```

>上面的这个例子中，`i` 只有在代码块中有效，在代码块外是无效的。

<br>
<br>


## 箭头函数

`ES6` 中增加了箭头函数，使得我们在编写 `Javascript` 的时候可以更加得心应手。


**我们来比较一下箭头函数和我们以往的函数写法有什么不一样**

* 以往的写法
```javascript
var fun = function(x){
    console.log(x)
}
var getNum = function(num){
    return num
}
var getText = function(){
    console.log(1)
}
```

<br>

* 箭头函数
```javascript
var fun = (x) => console.log(x)
var getNum = (num) => num;
var getText = () => console.log(1)      // 当没有参数的时候，需要保留括号
var fun = x => console.log(x);          //当函数只有一个的时候，可以省略括号
var getNum = num => num;
```


<br>
<br>

## 解构赋值


#### 什么是解构赋值

`解构赋值` 是一种 `javascript` 表达式。通过 `解构赋值` 可以将属性和值从对象或者数组中抽出，对应位置，赋值给其他变量。

<br>
<br>

#### 解构赋值怎么使用

* 以往我们的赋值是这样的
```javascript
var arr = ['1','2','3'];
var a = arr[0];     //'1'
var b = arr[1];     //'2'
var c = arr[2];     //'3'
```

<br>
<br>

* 有了解构赋值之后我们可以这样写
```javascript
let arr = ['1','2','3'];
let [a,b,c] = arr;
console.log(a);     //'1'
console.log(b);     //'2'
console.log(c);     //'3'
```

<br>
<br>

* 我们可以直接写成下面这种形式
```javascript
let [a,b,c] = ['1','2','3'];
console.log(a);     //'1'
console.log(b);     //'2'
console.log(c);     //'3'
```

<br>
<br>


* 嵌套数组的解构赋值
```javascript
let [a,[b],c] = ['1',['2'],'3']
console.log(b);             //['2']
let [a,b,c] = ['1',['2','2-1'],'3']
console.log(b);             //['2','2-1']
let [a,,c] = ['1','2','3'];
console.log(c) =            //'3'
let [a,b,c] = ['1',,'3'];
console.log(b)              //undefined, b 没有对应的值，输出 `undefined`
let [a,b,...c] = ['1'];
console.log(a)              //'1'
console.log(b)              //undefined, b 没有对应的值，输出 `undefined`
console.log(c)              //[]
```
>`...c` 表示 `reset参数` ，代表一个数组变量




<br>
<br>



## export

#### export一个变量

```javascript
var name = 'biu';

export default name;
//或者
export {name};
```

<br>
<br>

#### export多个变量

```javascript
var name = 'biu';
var age = 12;

export {name,age};
```


