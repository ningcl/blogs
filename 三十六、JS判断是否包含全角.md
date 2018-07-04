## JS判断是否包含全角

> #### JS判断是否包含全角

代码如下：

~~~
/**
 * JS判断是否包含全角
 * @param str
 */
function checkHasFull(str) {
    for ( var i = 0; i < str.length; i++) {
        strCode = str.charCodeAt(i);
        if ((strCode > 65248) || (strCode == 12288)) {
            return true;
            break;
        }
    }
    return false;
}

~~~

复制

调用方法：

~~~
checkHasFull("AaBb1234@#%&；，．：");    // true
checkHasFull("AaBb1234@#%&;,.:");       // false
~~~

