## JS判断是否以某个字符串开头

> #### 判断是否以某个字符串开头

代码如下：

~~~
/**
 * 判断是否以某个字符串开头
 * @param str 字符串
 * @param s 以哪个字符串开头
 * @returns {boolean} 返回true为正确，false为错误
 */
function startWith(str,s){
    return str.indexOf(s) == 0;
}

~~~

调用方法：

~~~
var test = "sdasd  sdx adsad asd sa ";
console.log(startWith(test,"a"));	//	例如：false
~~~

