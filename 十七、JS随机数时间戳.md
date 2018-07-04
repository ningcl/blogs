## JS随机数时间戳

> #### JS随机数时间戳

代码如下：

~~~
/**
 * JS随机数时间戳
 * @returns {string}
 */
function uniqueId(){
    var a=Math.random,b=parseInt;
    return Number(new Date()).toString()+b(10*a())+b(10*a())+b(10*a());
}

~~~

调用方法：

~~~
console.log(uniqueId());	// 例如：1525075670818519
~~~

