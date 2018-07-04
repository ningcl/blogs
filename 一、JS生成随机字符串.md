## 一、JS生成随机字符串

> #### 在创建订单时，我们希望订单号是唯一的，那么，则可能需要用到随机字符串+时间格式

### 代码如下：

~~~
/**
 * randomWord 产生任意长度随机字母数字组合
 * @param randomFlag 是否任意长度 min-任意长度最小位[固定位数] max-任意长度最大位
 * @param min
 * @param max
 * @returns {string}
 */
function randomWord(randomFlag, min, max){
    var str = "",
        range = min,
        arr = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9', 'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z'];

    // 随机产生
    if(randomFlag){
        range = Math.round(Math.random() * (max-min)) + min;
    }
    for(var i=0; i<range; i++){
        pos = Math.round(Math.random() * (arr.length-1));
        str += arr[pos];
    }
    return str;
}

~~~

### 调用方法

~~~
// 生成 3 - 32 位随即字符串
randomWord(true,3,32);  //  例如：olyOXUF5oDsuMmXl3Mi48
//  生成 32 位随机字符串
randomWord(false,32);   //  例如：fjpnWj29Bb8boiXbLeDF0nxkR4aYcLRl
~~~

