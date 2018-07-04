## JS数组去重

> #### 可以将数组中重复的部分去除掉

代码如下：

~~~
/**
 * JS数组去重
 * @param arr 数组
 * @returns {Array} 结果返回数组
 */
function removeReapt(arrs){
    var arr= [];
    var json = {};
    for(var i = 0,len = arrs.length; i < len; i++){
        if(!json[arrs[i]]){
            arr.push(arrs[i]);
            json[arrs[i]] = 1;
        }
    }
    return arr;
}

~~~

调用方法：

~~~
var arr = [11,22,33,46,79,11,46,97,79,46];
removeReapt(arr);
~~~

