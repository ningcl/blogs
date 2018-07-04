## JS获取前num天的日期

> #### JS获取前num天的日期

代码如下：

~~~
/**
 * JS获取前num天的日期
 * @param {Number} num 自动向上取整
 * @param {boolean} order true是日期从大到小，false是从小到大
 * @returns MM-dd
 */
function getTodayDate(num, order = false) {
    num = Math.ceil(num)
    let arr_Date = []
    for (var i = 0; i < num; i++) {
        let date = new Date(new Date().getTime() - (i * 24 * 60 * 60 * 1000))
        let currMonth = new Date(date).getMonth() + 1
        let currDay = new Date(date).getDate()
        let result = `${currMonth.toString().length < 2 ? `0${currMonth}` : currMonth}-${currDay.toString().length < 2 ? `0${currDay}` : currDay}`;
        if (order) {
            arr_Date.push(result);
        } else {
            arr_Date.unshift(result);
        }
    }
    return arr_Date;
}

~~~

复制

调用方法：

~~~
getTodayDate(7); 	// ["05-10", "05-11", "05-12", "05-13", "05-14", "05-15", "05-16"]
~~~

