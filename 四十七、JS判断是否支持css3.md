## JS判断是否支持css3

> #### JS判断是否支持css3

代码如下：

~~~
/**
 * JS判断是否支持css3
 * @param {string} style CSS属性
 * @returns
 */
function supportCss3(style) {
    var prefix = ['webkit', 'Moz', 'ms', 'o'],
        i,
        humpString = [],
        htmlStyle = document.documentElement.style,
        _toHumb = function (string) {
            return string.replace(/-(\w)/g, function ($0, $1) {
                return $1.toUpperCase();
            });
        };
    for (i in prefix)
        humpString.push(_toHumb(prefix[i] + '-' + style));
    humpString.push(_toHumb(style));
    for (i in humpString)
        if (humpString[i] in htmlStyle) return true;
    return false;
}

~~~

复制

调用方法：

~~~
supportCss3("transform");    // true
~~~

