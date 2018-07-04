## JS判断是否为空

> #### JS判断是否为空

代码如下：

~~~
/**
 * JS判断是否为空
 * @param val
 * @returns {boolean}
 */
function isNull(val) {
    if (val == undefined || val == null || val == "" || val == ''
        || val == "undefined" || val == "null" || val == "NULL") {
        return true;
    }
    return false;
}

~~~

复制

调用方法：

~~~
isNull(undefined);   	// true
isNull(null);   		// true
isNull(""); 			// true
isNull(''); 			// true
isNull("undefined");    // true
isNull("null"); 		// true
isNull("NULL");		    // true
~~~

