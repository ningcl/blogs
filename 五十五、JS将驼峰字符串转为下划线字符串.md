## S将驼峰字符串转为下划线字符串

> #### JS将驼峰字符串转为下划线字符串

代码如下：

~~~
/**
 * JS将驼峰字符串转为下划线字符串
 * @param str
 * @returns {*}
 */
function convertCamelCase(str) {
    if (typeof (str) != 'string') {
        console.error('[convertCamelCase] argument is not String.');
        return str;
    }
    var pattern = /[A-Z]/g;
    return str.replace(pattern, function(match, index) {
        if (index != 0) {
            return '_' + match.toLowerCase();
        } else {
            return match.toLowerCase();
        }
    });
}

~~~

复制

调用方法：

~~~
convertCamelCase("HelloWolrd");  // hello_wolrd
convertCamelCase(1);    // [convertCamelCase] argument is not String. 1
~~~

## JS检测是否支持transition

> #### JS检测是否支持transition

代码如下：

~~~
/**
 * JS检测是否支持transition
 * @returns {boolean}
 */
function supportTransition () {
    var s = document.createElement('p').style,
        r = 'transition' in s ||
            'WebkitTransition' in s ||
            'MozTransition' in s ||
            'msTransition' in s ||
            'OTransition' in s;
    s = null;
    return r;
}

~~~

复制

调用方法：

~~~
supportTransition(); // true
~~~

