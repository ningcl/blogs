## JS过滤字符串中所有空格

> #### JS过滤字符串中所有空格

代码如下：

~~~
/**
 * JS过滤字符串中所有空格
 * @param string
 * @returns {string}
 */
function ignoreSpaces(string) {
    var temp = "";
    string = '' + string;
    splitstring = string.split(" ");
    for(i = 0; i < splitstring.length; i++)
        temp += splitstring[i];
    return temp;
}

~~~

调用方法：

~~~
ignoreSpaces(" a b   c d e ");   // abcde
~~~

