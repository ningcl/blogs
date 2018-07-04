## JS判断是否为数字类型

> #### 判断是否为数字类型

代码如下：

~~~
/**
 * 判断是否为数字类型
 * @param value 判断的值
 * @returns {boolean}
 */
function isDigit(value) {
    var patrn = /^[0-9]*$/;
    if (patrn.exec(value) == null || value == "") {
        return false
    } else {
        return true
    }
}

~~~

调用方法：

~~~
var test = "5s";
var test2 = 5;
console.log(isDigit(test));		// false
console.log(isDigit(test2));	// true
~~~

