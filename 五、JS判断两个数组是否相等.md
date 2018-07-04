## JS判断两个数组是否相等

> #### 可以去判断两个数组是否相等

代码如下：

~~~
/**
 * JS判断两个数组是否相等
 * @param {Array} arr1
 * @param {Array} arr2
 * @returns {boolean} 返回true 或 false
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

调用方法：

~~~
var arr1 = ['a','b'];
var arr2 = ['a','b'];
arrayEqual(arr1,arr2);
~~~

