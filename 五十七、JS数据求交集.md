## JS数据求交集

> #### JS数据求交集

代码如下：

~~~
/**
 * JS数据求交集
 * @param array1
 * @param array2
 * @returns {*}
 */
function intersection(array1, array2) {
    return array1.filter(function(n) {
        return array2.indexOf(n) != -1;
    });
}

~~~

复制

调用方法：

~~~
var arr1 = [1,2,3,4,5];
var arr2 = [3,4,5,6,7];
intersection(arr1,arr2); // [3,4,5]
~~~

