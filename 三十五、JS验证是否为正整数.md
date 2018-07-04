## JS验证是否为正整数

> #### JS验证是否为正整数

代码如下：

~~~
/**
 * JS验证是否为正整数
 * @param str
 * @returns
 */
function checkNumber(str){
    return /^[1-9]\d*$/.test(str);
}

~~~

复制

调用方法：

~~~
checkNumber(100); 	// true
checkNumber(-100);  // false
~~~

