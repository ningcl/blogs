## JS XSS字符转义

> #### JS XSS字符转义

代码如下：

~~~
/**
 * JS XSS字符转义
 * @param markup
 * @returns {string}
 */
function replaceXSS(markup) {
    var _ENCODE_HTML_RULES = {
        "&": "&amp;",
        "<": "&lt;",
        ">": "&gt;",
        '"': "&#34;",
        "'": "&#39;"
    };
    var _MATCH_HTML = /[&<>'"]/g;

    function encode_char(c) {
        return _ENCODE_HTML_RULES[c] || c;
    };
    return markup === undefined ? '' : String(markup).replace(_MATCH_HTML, encode_char);
}

~~~

复制

调用方法：

~~~
replaceXSS("<>");    //  &lt;&gt;
~~~

