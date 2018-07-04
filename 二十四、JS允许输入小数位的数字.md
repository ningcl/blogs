## JS允许输入小数位的数字

> #### JS允许输入小数位的数字

代码如下：

~~~
/**
 * JS允许输入小数位的数字
 * @param curObj
 */
function clearNoFloat(curObj){
    curObj.value = curObj.value.replace(/[^\d.]/g,"");  //清除“数字”和“.”以外的字符
    curObj.value = curObj.value.replace(/^\./g,"");  //验证第一个字符是数字而不是.
    curObj.value = curObj.value.replace(/\.{2,}/g,"."); //只保留第一个. 清除多余的.
    curObj.value = curObj.value.replace(".","$#$").replace(/\./g,"").replace("$#$",".");
}

~~~

复制

调用方法：

~~~
<input type="text" onkeyup="clearNoFloat(this)"> // JS允许输入小数位，如果是其他字符，则会替换掉
~~~

