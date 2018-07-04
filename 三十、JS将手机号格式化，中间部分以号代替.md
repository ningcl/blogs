## JS将手机号格式化，中间部分以 * 号代替

> #### JS将手机号格式化，中间部分以 * 号代替

代码如下：

~~~
/**
 * JS将手机号格式化，中间部分以 * 号代替
 * @param phone
 * @returns {string | * | void}
 */
function phoneToStar( phone ) {
    return phone.replace(/(\d{3})\d{4}(\d{4})/, "$1****$2");
}

~~~

调用方法：

~~~
phoneToStar("16666666666");  // 166****6666
~~~

