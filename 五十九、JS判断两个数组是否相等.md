## JS Base64字符串编码与解码

> #### JS Base64字符串编码与解码

代码如下：

~~~
/**
 * JS判断两个数组是否相等
 * @param {Array} arr1
 * @param {Array} arr2
 * @return {Boolean}
 */
function arrayEqual(arr1, arr2) {
    if (arr1 === arr2) return true;
    if (arr1.length != arr2.length) return false;
    for (var i = 0; i < arr1.length; ++i) {
        if (arr1[i] !== arr2[i]) return false;
    }
    return true;
}

~~~

复制

调用方法：

~~~
var arr1 = [1,2,3,4,5];
var arr2 = [3,4,5,6,7];
var arr3 = [3,4,5,6,7];
var arr4 = [3,4,5,6,7];
arrayEqual(arr1,arr2);   // false
arrayEqual(arr3,arr4);   // true
~~~

