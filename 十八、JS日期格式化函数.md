## JS日期格式化函数

> #### JS日期格式化函数

代码如下：

~~~
/**
 * JS日期格式化函数
 * @param format 格式化格式
 * @returns {*}
 */
Date.prototype.format = function(format){
    var o = {
        "M+" : this.getMonth()+1, //month
        "d+" : this.getDate(),    //day
        "h+" : this.getHours(),   //hour
        "m+" : this.getMinutes(), //minute
        "s+" : this.getSeconds(), //second
        "q+" : Math.floor((this.getMonth()+3)/3),  //quarter
        "S" : this.getMilliseconds() //millisecond
    };
    if(/(y+)/.test(format)) format=format.replace(RegExp.$1,
        (this.getFullYear()+"").substr(4 - RegExp.$1.length));
    for(var k in o){
        if(new RegExp("("+ k +")").test(format))
            format = format.replace(RegExp.$1,RegExp.$1.length==1 ? o[k] :("00"+ o[k]).substr((""+ o[k]).length));
    }
    return format;
}

~~~

复制

调用方法：

~~~
console.log(new Date().format("yyyy-MM-dd hh:mm:ss"));	//	例如：2018-05-17 18:21:31
~~~

