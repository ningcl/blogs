## JS获取地址栏参数的值

> #### JS获取地址栏参数的值

代码如下：

~~~
/**
 * JS获取地址栏参数的值
 * @param name 对应的参数
 * @returns {*} 如果有，则返回参数值，没有则返回null
 */
function getUrlParam(name){
    var reg = new RegExp("(^|&)" + name + "=([^&]*)(&|$)");
    var r = window.location.search.substr(1).match(reg);
    if (r != null) {
        return unescape(r[2]);
    } else {
        return null;
    }
}

~~~

调用方法：

~~~
// 若当前的URL地址为：a.html?t1=1&t2=2&t3=3
console.log(getUrlParam("t1"));	// 1
~~~

