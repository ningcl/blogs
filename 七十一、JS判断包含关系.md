## JS判断包含关系

> #### JS判断包含关系

代码如下：

~~~
/**
 * JS判断包含关系
 * @param string 原始字符串
 * @param substr 子字符串
 * @param isIgnoreCase 忽略大小写
 * @returns {boolean}
 */
function jsContains(string,substr,isIgnoreCase)
{
    if(isIgnoreCase)
    {
        string=string.toLowerCase();
        substr=substr.toLowerCase();
    }
    var startChar=substr.substring(0,1);
    var strLen=substr.length;
    for(var j=0;j<string.length-strLen+1;j++)
    {
        if(string.charAt(j)==startChar)//如果匹配起始字符,开始查找
        {
            if(string.substring(j,j+strLen)==substr)//如果从j开始的字符与str匹配，那ok
            {
                return true;
            }
        }
    }
    return false;
}

~~~

复制

调用方法：

~~~
jsContains("Hello World!","world");          // false
jsContains("Hello World!","world",true);     // true
~~~

