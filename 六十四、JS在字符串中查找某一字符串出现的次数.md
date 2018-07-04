## JS在字符串中查找某一字符串出现的次数

> #### JS在字符串中查找某一字符串出现的次数

代码如下：

~~~
/**
 * JS在字符串中查找某一字符串出现的次数
 * @param str
 * @param strSplit
 * @returns {number}
 */
function countStr (str,strSplit){
    return str.split(strSplit).length-1
}

~~~

复制

调用方法：

~~~
var strTest='sad44654blog5a1sd67as9dablog4s5d16zxc4sdweasjkblogwqepaskdkblogahseiuadbhjcibloguyeajzxkcabloguyiwezxc967'
countStr(strTest,"blog");    // 6
~~~

