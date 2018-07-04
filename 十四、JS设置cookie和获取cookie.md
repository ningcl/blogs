## JS设置cookie和获取cookie

> #### 设置cookie和获取cookie

代码如下：

设置 Cookie：

~~~
/**
 * 设置cookie值
 * setCookie（键，值，保存时长（毫秒））
 * @param name cookie对应名字
 * @param value 该cookie对应的值
 * @param Hours
 */
function setCookie(name, value, expiredays) {
    var exdate = new Date();
    exdate.setTime(Number(exdate) + expiredays);
    document.cookie = name + "=" + escape(value) + ((expiredays == null) ? "" : ";expires=" + exdate.toGMTString());
}

~~~

获取 Cookie：

~~~
/**
 * JS 获取 Cookie
 * @param name cookie对应名字
 * @returns {string}
 */
function getCookie(name) {
    if(document.cookie.length > 0) {
        c_start = document.cookie.indexOf(name + "=");//获取字符串的起点
        if(c_start != -1) {
            c_start = c_start + name.length + 1;//获取值的起点
            c_end = document.cookie.indexOf(";", c_start);//获取结尾处
            if(c_end == -1) c_end = document.cookie.length;//如果是最后一个，结尾就是cookie字符串的结尾
            return decodeURI(document.cookie.substring(c_start, c_end));//截取字符串返回
        }
    }
    return "";
}

~~~

复制

调用方法：

~~~
setCookie("zhangshan", "name1", 20*1000);
setCookie("lisi", "name2");

console.log(getCookie("zhangshan"));		//	name1
console.log(getCookie("lisi"));				//	name2
~~~

