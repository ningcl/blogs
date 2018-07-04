## JS替换非法字符

> #### JS替换非法字符

代码如下：

~~~
/**
 * JS替换非法字符
 * @param sStr
 * @returns {string}
 * @constructor
 */
function URLencode(sStr) {
    return escape(sStr).replace(/\+/g, '%2B').replace(/\"/g, '%22').replace(/\'/g, '%27').replace(/\//g, '%2F');
}

~~~

复制

调用方法：

~~~
URLencode("=");  // %3D
~~~

