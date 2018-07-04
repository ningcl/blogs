## JS完美判断是否为网址

> #### JS完美判断是否为网址

代码如下：

~~~
/**
 * JS完美判断是否为网址
 * @param strUrl URL地址
 * @returns {boolean} 返回真或者假
 * @constructor
 */
function IsURL(strUrl) {
    var regular = /^\b(((https?|ftp):\/\/)?[-a-z0-9]+(\.[-a-z0-9]+)*\.(?:com|edu|gov|int|mil|net|org|biz|info|name|museum|asia|coop|aero|[a-z][a-z]|((25[0-5])|(2[0-4]\d)|(1\d\d)|([1-9]\d)|\d))\b(\/[-a-z0-9_:\@&?=+,.!\/~%\$]*)?)$/i
    if (regular.test(strUrl)) {
        return true;
    }else {
        return false;
    }
}

~~~

调用方法：

~~~
console.log(IsURL("https://www.notelist.cn"));	// true
~~~

