## JS从数组中随机获取元素

> #### JS从数组中随机获取元素

代码如下：

~~~
/**
 * JS从数组中随机获取元素
 * @param arr
 * @returns {*}
 */
function randomOne(arr) {
    return arr[Math.floor(Math.random() * arr.length)];
}

~~~

复制

调用方法：

~~~
var arr = [1,2,3,4,5,6,7,8,9,0];
randomOne(arr);  //  9
~~~

