## JS验证密码，必须是字母和数字结合

> #### JS验证密码，必须是字母和数字结合

代码如下：

~~~
/**
 * JS验证密码，必须是字母和数字结合
 * @param password 密码
 * @returns {boolean} 返回true或false
 */
function checkPasswordValidate(password) {
    return /^(?!^\d+$)(?!^[a-zA-Z]+$)[0-9a-zA-Z]{6,20}$/.test(password);
}

~~~

复制

调用方法：

~~~
checkPasswordValidate("dasdas1132156");  // true
checkPasswordValidate("dsadasdas"); 	 // false
~~~

