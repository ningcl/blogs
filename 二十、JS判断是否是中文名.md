## JS判断是否是中文名

> #### JS判断是否是中文名

代码如下：

~~~
/**
 * JS判断是否是中文名
 * @param value
 * @returns {boolean}
 */
function isChinese(value){
    var reg = /^[\u4e00-\u9fa5]+$/i;
    if (!reg.test(value))
    {
        //  不是中文名
        return false;
    }
    //  是中文名
    return true;
}

~~~

复制

调用方法：

~~~
console.log(isChinese("牛逼"));	// true
~~~

