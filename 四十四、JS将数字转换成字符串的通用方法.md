## S将数字转换成字符串的通用方法

> #### JS将数字转换成字符串的通用方法

代码如下：

~~~
/**
 * JS将数字转换成字符串的通用方法
 * 说明:直接使用 toFixed 方法会进行四舍五入，因此写一个将数字转换为指定小数位数字符串的方法
 * @param sourceData 源数据
 * @param decimalLen 小数的位数
 */
function numberToString(sourceData, decimalLen)
{
    decimalLen = typeof(decimalLen) == undefined ? 0 : decimalLen;
    var result = sourceData + "";
    var integerStr = null; // 整数部分
    var decimalStr = null; // 小数部分
    if(result.indexOf(".") == -1)
    {
        result = Number(result).toFixed(decimalLen);
    }
    else
    {
        integerStr = result.substring(0, result.indexOf(".")); // 整数部分
        decimalStr = /\.\d+/.exec(result); // 小数部分
        decimalStr = Number(decimalStr);
        decimalStr = decimalStr.toPrecision(decimalLen).substr(0, decimalLen + 2);
        result = integerStr + decimalStr.substr(1);
    }
    return result;
}

~~~

复制

调用方法：

~~~
numberToString(233,2);   // 233.00
~~~

