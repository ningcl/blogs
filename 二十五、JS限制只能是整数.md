## JS限制只能是整数

> #### JS限制只能是整数

代码如下：

~~~
/**
 * JS限制只能是整数，不能是小数
 * @param curObj
 */
function clearNoInt(curObj){
    curObj.value = curObj.value.replace(/[^\d]/g,"");  //清除“数字”和“.”以外的字符
}

~~~

调用方法：

~~~
<input type="text" onkeyup="clearNoInt(this)">
~~~

