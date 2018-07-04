## JS校验Ip地址格式

> #### JS校验Ip地址格式

代码如下：

~~~
/**
 * JS校验Ip地址格式
 * @param ipvale
 * @returns {boolean}
 */
function checkIp(ipvale) {
    var regex = /^([1-9]|[1-9]\d|1\d{2}|2[0-1]\d|22[0-3])(\.(\d|[1-9]\d|1\d{2}|2[0-4]\d|25[0-5])){3}$/;
    var b = regex.test(ipvale);
    return b;
}

~~~

复制

调用方法：

~~~
checkIp("127.0.0.1");    // true
checkIp("0.0.0.1");      // false
~~~

