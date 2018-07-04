## S检查输入的一串字符是否全部是英文

> #### JS检查输入的一串字符是否全部是英文

代码如下：

~~~
/**
 * JS检查输入的一串字符是否全部是英文
 * @param str 字符串
 * @returns true 或 false; true表示为数字或者英文
 */
function checkEnDashOrSpace(str) {
    for ( var i = 0; i < str.length; i++) {
        var strTmp = str.charAt(i);
        if (!(/[A-Za-z]/.test(strTmp))) {
            return false;
        }
    }
    return true;
}

~~~

复制

调用方法：

~~~
checkEnDashOrSpace("dasdasda1"); 	// false
checkEnDashOrSpace("ddlkjasd"); 	// true
~~~

