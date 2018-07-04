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

