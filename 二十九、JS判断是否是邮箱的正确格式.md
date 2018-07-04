## JS判断是否是邮箱的正确格式

> #### JS判断是否是邮箱的正确格式

代码如下：

~~~
/**
 * 判断是否是邮箱的正确格式
 * @param str 对应的需要验证的邮箱地址
 * @returns {boolean} 返回真或假
 */
function isEmail(str) {
    var emailRegx = /^([a-z0-9A-Z]+[-|\.]?)+[a-z0-9A-Z]@([a-z0-9A-Z]+(-[a-z0-9A-Z]+)?\.)+[a-zA-Z]{2,}$/;
    return emailRegx.test(str);
}

~~~

复制

调用方法：

~~~
isEmail("ye21st@gmail.com");	// true
isEmail("ye21st!gmail.com");	// false
~~~

