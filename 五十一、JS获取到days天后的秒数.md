## JS获取到 days 天后的秒数

> #### JS获取到 days 天后的秒数

代码如下：

~~~
/**
 * JS获取到 days 天后的秒数
 * @param days
 * @returns {number}
 */
function getSurplusSeconds(days){
    days = days || 0;
    var d = new Date();
    var str1 = d.getTime();
    d.setHours(23, 59, 59);
    var str2 = d.getTime();
    return (str2 - str1)/1000 + days * 86400;
}

~~~

复制

调用方法：

~~~
getSurplusSeconds(2);    // 191592
~~~

