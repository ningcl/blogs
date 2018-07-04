## JS适配rem

> #### JS适配rem

代码如下：

~~~
/**
 * JS适配rem
 */
function getFontSize(){
    var doc=document,win=window;
    var docEl = doc.documentElement,
        resizeEvt = 'orientationchange' in window ? 'orientationchange' : 'resize',
        recalc = function () {
            var clientWidth = docEl.clientWidth;
            if (!clientWidth) return;
            //如果屏幕大于750（750是根据我效果图设置的，具体数值参考效果图），就设置clientWidth=750，防止font-size会超过100px
            if(clientWidth>750){clientWidth=750}
            //设置根元素font-size大小
            docEl.style.fontSize = 100 * (clientWidth / 750) + 'px';
        };
    //屏幕大小改变，或者横竖屏切换时，触发函数
    win.addEventListener(resizeEvt, recalc, false);
    //文档加载完成时，触发函数
    doc.addEventListener('DOMContentLoaded', recalc, false);
}

~~~

调用方法：

~~~
getFontSize();

<style>
    /*使用方式很简单，比如效果图上，有张图片。宽高都是100px;*/
    /*样式写法就是*/
      img{
          width:1rem;
          height:1rem;
      }
    /*这样的设置，比如在屏幕宽度大于等于750px设备上，1rem=100px；图片显示就是宽高都是100px*/
    /*比如在iphone6(屏幕宽度：375)上，375/750*100=50px;就是1rem=50px;图片显示就是宽高都是50px;*/
</style>
~~~

