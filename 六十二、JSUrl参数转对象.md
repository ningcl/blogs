## JS Url参数转对象

> #### JS Url参数转对象

代码如下：

~~~
/**
 * JS Url参数转对象
 * @param  {String} url  default: window.location.href
 * @return {Object}
 */
function parseQueryString(url) {
    url = url == null ? window.location.href : url
    var search = url.substring(url.lastIndexOf('?') + 1)
    if (!search) {
        return {}
    }
    return JSON.parse('{"' + decodeURIComponent(search).replace(/"/g, '\\"').replace(/&/g, '","').replace(/=/g, '":"') + '"}')
}

~~~

复制

调用方法：

~~~
parseQueryString("http://www.baidu.com?id=1&name=ye21st");   // {id: "1", name: "ye21st"}
~~~

