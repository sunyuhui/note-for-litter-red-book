## 《函数表达式》

###立即执行函数的原理

立即执行函数通常是这样的：

	(function getName(){
		console.log('sunyuhui');
	})()

为啥这样写可以运行呢？先把立即执行函数拆解一下：由两对括号组成，在第一个括号里有一个函数申明

首先，我们知道加一对括号`()`（也就是上面例子中的第二对括号）是用来执行函数的。比如我们用函数表达式申明一个函数

	var getName = function(){
		console.log('sunyuhui');
	}
	getName() //这样就可以执行getName这个函数


那第一段代码里面的**一对括号里面包含一个函数申明**是为啥呢？其实是**为了把函数申明转换成函数表达式**（这一点才是立即执行函数能够执行的主要原因），所以第一对括号以及括号里的内容其实就是一个**函数表达式**。

问：那为啥不直接写一个函数申明呢？比如这样：

	function getName(){
		console.log('sunyuhui');
	}()

答：因为这样会报错，函数申明后面不能跟括号