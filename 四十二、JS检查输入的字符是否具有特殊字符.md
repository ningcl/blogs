## JS检查输入的字符是否具有特殊字符

> #### JS检查输入的字符是否具有特殊字符

代码如下：

~~~
/**
 * JS检查输入的字符是否具有特殊字符
 * @param str 字符串
 * @returns true 或 false; true表示包含特殊字符 主要用于注册信息的时候验证
 */
function checkQuote(str) {
    var items = new Array("~", "`", "!", "@", "#", "$", "%", "^", "&", "*", "{", "}", "[", "]", "(", ")");
    items.push(":", ";", "'", "|", "\\", "<", ">", "?", "/", "<<", ">>", "||", "//");
    items.push("select", "delete", "update", "insert", "create", "drop", "alter", "trancate");
    str = str.toLowerCase();
    for ( var i = 0; i < items.length; i++) {
        if (str.indexOf(items[i]) >= 0) {
            return true;
        }
    }
    return false;
}

~~~

复制

调用方法：

~~~
checkQuote("dasd1!/,/.");    // true
checkQuote("52014sdsda");    // false
~~~

