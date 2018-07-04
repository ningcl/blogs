## JS获取页面高度

> #### 获取页面高度

代码如下：

~~~
/**
 * 获取页面高度
 * @returns {number} 返回对应高度数值
 */
function getPageHeight(){
    var g = document, a = g.body, f = g.documentElement, d = g.compatMode == "BackCompat"
        ? a
        : g.documentElement;
    return Math.max(f.scrollHeight, a.scrollHeight, d.clientHeight);
}

~~~

调用方法：

~~~
console.log(getPageHeight());   // 例如：255
~~~

