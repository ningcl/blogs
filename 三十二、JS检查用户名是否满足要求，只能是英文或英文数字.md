## JS检查用户名是否满足要求，只能是英文或英文数字

> #### JS检查用户名是否满足要求，只能是英文或英文数字

代码如下：

~~~
/**
 * JS检查用户名是否满足要求，只能是英文或英文数字
 * @returns {*}
 */
function checkLoginName(loginName) {
    return /^[A-Za-z0-9]*$/.test(loginName) && !/(^\d*$)|(^\S+\s+\S+$)/.test(loginName);
}

~~~

复制

调用方法：

~~~
checkLoginName("ye21st");    // true
checkLoginName("sam!"); 	 // false
~~~

