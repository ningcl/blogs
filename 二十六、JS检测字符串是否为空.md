## JS检测字符串是否为空

> #### JS检测字符串是否为空

代码如下：

~~~
/**
 * JS检测字符串是否为空
 * @param str
 * @returns {boolean}
 */
function checkIsEmpty(str) {
    if (null != str && undefined != str && "" != str) {
        return false;
    }
    return true;
}

~~~

复制

调用方法：

~~~
console.log(checkIsEmpty(""));	//	true
~~~

