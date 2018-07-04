## JS切割相应小数点后位数，并将小数点后多余的0 清空

> #### JS切割相应小数点后位数，并将小数点后多余的0 清空

代码如下：

~~~
/**
 * 切割相应小数点后位数，并将小数点后多余的0 清空
 * @param value 需要切割的数值
 * @param num 需要的小数位数
 * @returns {string}
 */
function cutRoundNum( value , num ) {
    var value = value.toString();
    value =  value.substr(0,value.indexOf('.')+1) + value.substr(value.indexOf('.')+1,num);

    var regx = value.match(/\d+\.\d+/g);
    for ( var index in regx) {
        value = value.replace(regx[index],parseFloat(regx[index]));
    }
    return value;
}

~~~

复制

调用方法：

~~~
cutRoundNum(2.333000,4); 	// 2.333
~~~

