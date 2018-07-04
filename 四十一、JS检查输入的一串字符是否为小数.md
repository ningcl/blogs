## JS检查输入的一串字符是否为小数

> #### JS检查输入的一串字符是否为小数

代码如下：

~~~
/**
 * JS检查输入的一串字符是否为小数
 * @param str 字符串
 * @returns true 或 false; true表示为小数
 */
function checkDecimal(str) {
    if (str.match(/^-?\d+(\.\d+)?$/g) == null) {
        return false;
    } else {
        return true;
    }
}

~~~

复制

调用方法：

~~~
checkDecimal("51a.dad12");   // false
checkDecimal("2.3333");      // true
~~~

