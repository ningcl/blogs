## JS判断浏览器

> #### JS判断浏览器

代码如下：

~~~
/**
 * JS手机类型判断
 * @type {{userAgent: string, isAndroid: boolean, isIphone: boolean, isIpad: boolean, isWeixin: boolean, isChrome: boolean}}
 */
var BrowserInfo = {
    userAgent: navigator.userAgent.toLowerCase(),
    isAndroid: Boolean(navigator.userAgent.match(/android/ig)),
    isIphone: Boolean(navigator.userAgent.match(/iphone|ipod/ig)),
    isIpad: Boolean(navigator.userAgent.match(/ipad/ig)),
    isWeixin: Boolean(navigator.userAgent.match(/MicroMessenger/ig)),
    isChrome:Boolean(navigator.userAgent.match(/chrome/ig)),
}

~~~

复制

调用方法：

~~~
BrowserInfo; // android
~~~

