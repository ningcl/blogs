## JS字符串反序

> #### JS字符串反序

代码如下：

~~~
/**
 * JS字符串反序
 * @param text 需要进行反序的字符串
 * @returns {string} 返回反序之后的字符串
 * @constructor
 */
function IsReverse(text){
    return text.split('').reverse().join('');
}

~~~

复制

调用方法：

~~~
console.log(IsReverse("Hello!"));	//	!olleH
~~~

