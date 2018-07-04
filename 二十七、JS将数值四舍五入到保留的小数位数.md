## JS将数值四舍五入到保留的小数位数

> #### JS将数值四舍五入到保留的小数位数

代码如下：

~~~
/**
 * 将数值四舍五入到保留的小数位数
 * @param num 待四舍五入数值
 * @param len 保留小数位数
 * @returns {number}
 */
function getRound(num,len) {
    return Math.round(num * Math.pow(10, len)) / Math.pow(10, len);
}

~~~

复制

调用方法：

~~~
getRound(6.123456,4); // 6.1235
~~~

