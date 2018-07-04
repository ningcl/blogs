## JS Base64字符串编码与解码

> #### JS Base64字符串编码与解码

代码如下：

~~~
/**
 * BASE64加密
 * @param str
 * @returns {string}
 */
function base64Encode(str) {
    return btoa(unescape(encodeURIComponent(str)));
}

/**
 * BASE64解密
 * @param str
 * @returns {string}
 */
function base64Decode(str) {
    return decodeURIComponent(escape(atob(str)));
}

~~~

复制

调用方法：

~~~
base64Encode("test");    // dGVzdA==
base64Decode(test);     // test
~~~

