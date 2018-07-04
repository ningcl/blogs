## JS判断浏览器

> #### JS判断浏览器

代码如下：

~~~
/**
 * JS判断浏览器
 * @returns {string}
 */
function getOs() {
    if (navigator.userAgent.indexOf("MSIE 8.0") > 0) {
        return "MSIE8";
    } else if (navigator.userAgent.indexOf("MSIE 6.0") > 0) {
        return "MSIE6";
    } else if (navigator.userAgent.indexOf("MSIE 7.0") > 0) {
        return "MSIE7";
    } else if (isFirefox = navigator.userAgent.indexOf("Firefox") > 0) {
        return "Firefox";
    }
    if (navigator.userAgent.indexOf("Chrome") > 0) {
        return "Chrome";
    } else {
        return "Other";
    }
}

~~~

复制

调用方法：

~~~
getOs(); // Chrome
~~~

