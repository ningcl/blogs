## JS检查输入的邮政编码是否正确

> #### JS检查输入的邮政编码是否正确

代码如下：

~~~
/**
 * JS检查输入的邮政编码是否正确
 * @param str
 * @returns {Boolean}
 */
function checkPostcode(str){
    if (str.match(/^[1-9][0-9]{5}$/) == null) {
        return false;
    } else {
        return true;
    }
}

~~~

复制

调用方法：

~~~
checkPostcode("423000"); 	// true
checkPostcode("029000"); 	// false
~~~

