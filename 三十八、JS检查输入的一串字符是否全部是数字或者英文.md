## JS检查输入的一串字符是否全部是数字或者英文

> #### JS检查输入的一串字符是否全部是数字或者英文

代码如下：

~~~
/**
 * JS检查输入的一串字符是否全部是数字或者英文
 * @param str 字符串
 * @returns true 或 false; true表示为数字或者英文
 */
function checkEnNum(str) {
    for ( var i = 0; i < str.length; i++) {
        var strTmp = str.charAt(i);
        if (!(/[A-Za-z0-9]/.test(strTmp))) {
            return false;
        }
    }
    return true;
}

~~~

复制

调用方法：

~~~
checkEnNum("dasdasdas"); 		// true
checkEnNum("dasdasdas13615!");  // false
~~~

