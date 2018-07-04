## JS判断是否以某个字符串结束

> #### 判断是否以某个字符串结束

代码如下：

~~~
/**
 * 判断是否以某个字符串结束
 * @param str 总字符串
 * @param s 某个字符串
 * @returns {boolean}
 */
function endWith(str,s){
    var d = str.length - s.length;
    return (d >= 0 && str.lastIndexOf(s) == d);
}

~~~

调用方法：

~~~
var test = "sdasd  sdx adsad asd sa";
console.log(endWith(test,"a"));	//	例如:true
~~~

