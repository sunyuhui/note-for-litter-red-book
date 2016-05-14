####关于注释

/*   这里是注释
 *   这里是注释
 *   这里是注释
 */

 上面第二个星号和第三个星号其实不是必须的，只是为了提高可读性才加的，位于`/*`和`*/`之间的所有内容都会被当做注释

 ####关于变量

 JavaScript中每个变量都是一个指针，指向内存中某个地址，**null**是**空对象指针**，所以使用`typeof null`会返回`object`

 ####浮点数的算术操作

 浮点数（包含小数点，且小数点后至少有一位数）的最高精度是17位小数，但在进行算术计算时精度非常差劲。

 比如：

 console.log(0.1 + 0.2)   // 0.30000000000000004

 console.log(0.3 - 0.2)   // 0.09999999999999998

 so，使用浮点数精心计算的时候最好多注意 ~ 

 ####每个对象都有的属性和方法

 **一切皆对象**，在JavaScript中所有变量通过原型链最终都能找到构造函数(Object)，因此所有变量(除了undefined和null）都有Object所具有的属性和方法

 1. constructor
 2. hasOwnproperty(propertyName)
 3. isPrototypeOf(object)
 4. propertyIsEnumerable(propertyName)
 5. toLocaleString()
 6. toString()
 7. valueOf()

 注意：上面说的是【所有变量】，比如字符串、数字或者数组等。。

