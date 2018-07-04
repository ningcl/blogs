## JS忽略大小写判断字符串是否相同

> #### JS忽略大小写判断字符串是否相同

代码如下：

~~~
/**
 * JS忽略大小写判断字符串是否相同
 * @param str1
 * @param str2
 * @returns {boolean}
 */
function isEqualsIgnorecase(str1,str2) {
    if(str1.toUpperCase() == str2.toUpperCase()){
        return true;
    }else{
        return false;
    }
}

~~~

复制

调用方法：

~~~
isEqualsIgnorecase("abc","ABC"); 	// true
~~~

