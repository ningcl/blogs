## JS 将object转为form data，方便post提交

> #### JS 将object转为form data，方便post提交

代码如下：

~~~
/**
 * JS 将object转为form data，方便post提交
 * @param {Object} obj [数据对象]
 * @return {String}
 */
function encodeFormData(obj) {
    if (!obj) return;
    var pairs = [];
    for (var name in obj) {
        if (!obj.hasOwnProperty(name)) continue;
        if (typeof obj[name] == 'function') continue;
        var value = obj[name].toString();
        name = encodeURIComponent(name.replace('%20', '+'));
        value = encodeURIComponent(value.replace('%20', '+'));
        pairs.push(name + '=' + value);
    }
    return pairs.join('&');
}

~~~

复制

调用方法：

~~~
encodeFormData({"id":1,"name":"ye21st"});    // id=1&name=ye21st
~~~

