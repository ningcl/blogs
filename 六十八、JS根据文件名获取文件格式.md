## JS根据文件名获取文件格式

> #### JS根据文件名获取文件格式

代码如下：

~~~
/**
 * JS根据文件名获取文件格式
 * @param str
 * @returns {string}
 */
function getFileTypeByFileName(str){
    return str.substr(str.lastIndexOf(".")+1).toLowerCase();
}

~~~

复制

调用方法：

~~~
getFileTypeByFileName("index.html"); 	// html
getFileTypeByFileName("index.js");  	// js
getFileTypeByFileName("index.php"); 	// php
~~~

