## S生成UUID

> #### 很多时候，我们需要保证标识符唯一，那么，使用UUID是你不错的选择。

代码如下：

~~~
/**
 * generateUUID 生成UUID
 * @returns {string} 返回字符串
 */
function generateUUID(){
    var d = new Date().getTime();
    var uuid = 'xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx'.replace(/[xy]/g, function(c) {
        var r = (d + Math.random()*16)%16 | 0;
        d = Math.floor(d/16);
        return (c=='x' ? r : (r&0x7|0x8)).toString(16);
    });
    return uuid;
}

~~~

调用方法：

~~~
generateUUID();	// 例如：7ceb31a7-41b9-45ed-915b-14c7ad0fddf6
~~~

