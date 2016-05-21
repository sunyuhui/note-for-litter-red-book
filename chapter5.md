##《引用类型》

####数组的`indexOf()` 和 `lastIndexOf()`在查找元素时使用的是严格相等

	var arr = [1, '23'];
	console.log(arr.indexOf(23));   // -1
	console.log(arr.indexOf('23'));  // 1

我以前只知道`switch()`用的是严格相等，原来`indexOf()`和`lastIndexOf()`也用的严格相等


####为什么不能为基本引用类型添加属性或方法

我以前的理解是基本类型并不是对象，所以就不能添加属性和方法，但是这只是浅层原因.

深层原因是：还是用例子来说明吧

	var name = 'sunyuhui';
	console.log(name.toString());

上面创建了一个字符串，按理来说，基本类型值不是对象，是不会有方法的，那为什么可以使用`toString()`方法呢？而且我们都知道`toString()`方法来自于对`Object`的继承，

原因是由于看起来我们只是创建了一个字符串，但JS引擎会自动创建一个对应的**基本包装类型的对象**，类似于这样：

	var name = new String('sunyuhui');
	name  = null;

上面是创建完就销毁了，如果我们添加一些操作。

	var name = 'sunyuhui';
	var anotherName = name.slice(0,3);

在执行时JS引擎就是这样执行的：

	var name = new String('sunyuhui');
	var anotherName = name.slice(0,3);
	name = null;

操作完之后就销毁了。

如果我们给基本类型值添加属性的话会怎样呢？

	var name = 'sunyuihui';
	name.age = 18;
	console.log(name.age);    //undefined

那JS引擎在执行时会怎样呢？

	var name = new String('sunyuhui');
	name.age = 18;
	name = null;

所以在上面访问`name.age`是才会undefined.

	


