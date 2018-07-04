## JS格式化金额

> #### 可以将金额进行格式化

代码如下：

~~~
/**
 * JS格式化金额
 * @param money
 * @param type
 * @returns {*}
 */
function convert(money , type) {
    if (/[^0-9\.]/.test(money))
        return "0";
    if (money == null || money == "")
        return "0";
    money = money.toString().replace(/^(\d*)$/, "$1.");
    money = (money + "00").replace(/(\d*\.\d\d)\d*/, "$1");
    money = money.replace(".", ",");
    var re = /(\d)(\d{3},)/;
    while (re.test(money))
        money = money.replace(re, "$1,$2");
    money = money.replace(/,(\d\d)$/, ".$1");
    if (type == 0) {// 不带小数位(默认是有小数位)
        var a = money.split(".");
        if (a[1] == "00") {
            money = a[0];
        }
    }
    return money;
}

~~~

调用方法：

~~~
convert(311546161685);  //  311,546,161,685.00
convert(311546161685,0);  //  311,546,161,685
~~~

