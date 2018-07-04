## JS字符串长度截取

> #### 可以将字符串的长度进行截取

代码如下：

~~~
/**
 * 字符串长度截取
 * @param str 给定的字符串
 * @param len 给定的长度
 * @returns {string} 返回截取之后的字符串
 */
function cutStr(str, len) {
    var temp,
        icount = 0,
        patrn = /[^\x00-\xff]/,
    strre = "";
    for (var i = 0; i < str.length; i++) {
        if (icount < len - 1) {
            temp = str.substr(i, 1);
            if (patrn.exec(temp) == null) {
                icount = icount + 1
            } else {
                icount = icount + 2
            }
            strre += temp
        } else {
            break;
        }
    }
    return strre + "..."
}

~~~

调用方法：

~~~
var str = "fhasjdhklsajhfnolsai";
console.log(cutStr(str,8));	//	例如：fhasjdh...
~~~

