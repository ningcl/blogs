## JS检查输入的一串字符是否全部是数字

> #### JS检查输入的一串字符是否全部是数字

代码如下：

~~~
/**
 * JS检查输入的一串字符是否全部是数字
 * @param str 字符串
 * @returns true 或 false; true表示为数字
 */
function checkNum(str) {
    if (checkHasFull(str)) {
        return false;
    }
    return str.match(/\D/) == null;
}

/**
 * JS判断是否包含全角
 * @param str
 */
function checkHasFull(str) {
    for ( var i = 0; i < str.length; i++) {
        strCode = str.charCodeAt(i);
        if ((strCode > 65248) || (strCode == 12288)) {
            return true;
            break;
        }
    }
    return false;
}

~~~

调用方法：

~~~
checkNum("21315，．：");    // false
checkNum("489641"); 		// true
~~~

