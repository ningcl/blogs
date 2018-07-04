## JS验证手机格式

> #### 很多时候，我们需要在JS当中去验证手机格式是否正确

代码如下：

~~~
/**
 * @param str 对应手机号码
 * @returns {boolean} 结果返回 true 和 false。
 * true 为正确手机号码
 * false 为错误手机号码
 */
function verifyPhoneNumberFormat(str){
    var myreg = /^(((13[0-9]{1})|(15[0-9]{1})|(17[0-9]{1})|(18[0-9]{1}))+\d{8})$/;
    return myreg.test(str);
}

~~~

复制

调用方法：

~~~
verifyPhoneNumberFormat("18818592555");
~~~

