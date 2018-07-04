## S获取到 days 天后的秒数

> #### JS获取到 days 天后的秒数

代码如下：

~~~
/**
 * JS生成从minNum到maxNum的随机整数
 * @param {number} minNum
 * @param {number} maxNum
 * @param {boolean} [status=true] 生成整数 false生成小数
 * @returns
 */
function randomNum(minNum, maxNum, status = true) {
    let result;
    switch (arguments.length) {
        case 1:
            result = parseInt(Math.random() * minNum + 1, 10);
            break
        case 2:
            result = parseInt(Math.random() * (maxNum - minNum + 1) + minNum, 10);
            break
        case 3:
            if (status) {
                result = parseInt(Math.random() * (maxNum - minNum + 1) + minNum, 10);
                break
            } else {
                result = Math.random() * (maxNum - minNum + 1) + minNum;
                break
            }
        default:
            result = 0;
            break
    }
    return result;
}

~~~

复制

调用方法：

~~~
randomNum(1,1000,false); // 177.70599277153732
randomNum(1,1000); 		 // 246
~~~

