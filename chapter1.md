##《JavaScript简介》

###最大收获：重新梳理了JavaScript的来源。

直接说结论：

![chapter1](img/chapter1.jpg)

上图表明：**JavaScript**并不是一门新语言，它是由**ECMAScript**、**DOM**、**BOM**组成的。

####ECMAScript

我们通常把**JavaScript**当做一门语言，但其实**JavaScript**这门语言中的那些**语法，数据类型、函数**都是从ECMAScript里拿来的，所以严格来说：ECMAScript才是一门语言。

ECMAScript是有标准的，就是我们通常说的ES5，ES6。目前（2016）来说，现在各主流浏览器对ES5的支持是非常好的，ES6还没有被广泛支持。

####DOM

问：DOM是什么？

答：文档对象模型，对，我们都知道DOM是**Document Object Module**，但这么说太官方了，对我们理解并没有什么帮助。

再给一次机会： DOM其实就是API，这套API主要的用处是用来操作HTML页面上的节点。比如其中一个API是**getElementById()**

DOM也是有标准的，也就是我们说的DOM1级，DOM2级，现在各主流浏览器对DOM2级的支持也是很好的，这一点不会存在什么问题。

####BOM

BOM是没有标准的，正是由于没有标准，所以浏览器们各做各的，这也就是【浏览器兼容问题】的根源（并不是说兼容问题只存在与BOM，DOM里也有一些兼容问题），不过好在HTML5是有规范的，HTML5定义了BOM的一些标准，有了标准，各浏览器就能按照这个标准来了，目前浏览器们对HTML5的支持还是非常好的。

注：上面提到的浏览器对标准的支持程度说的很模糊，这是因为各浏览器很少会把标准里的东西全部支持，通常是有些属性支持的很好，有些支持的不太好，对某一个具体的属性支持程度可以上[Caniuse.com](http://caniuse.com/)查询。可以查询HTML5、Css、JS。

END