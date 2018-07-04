## JS获取当前时间

> #### JS获取当前时间

代码如下：

~~~
/**
 * JS获取当前时间
 * @returns {string}
 * @constructor
 */
function GetCurrentDate() {
    var d = new Date();
    var y = d.getYear() + 1900;
    month = add_zero(d.getMonth() + 1),
        days = add_zero(d.getDate()),
        hours = add_zero(d.getHours());
    minutes = add_zero(d.getMinutes()),
        seconds = add_zero(d.getSeconds());
    var str = y + '-' + month + '-' + days + ' ' + hours + ':' + minutes + ':' + seconds;
    function add_zero(temp) {
        if (temp < 10){
            return "0" + temp;
        }
        return temp;
    }
    return str;
}

~~~

复制

调用方法：

~~~
GetCurrentDate();    // 2018-05-16 18:30:49
~~~

