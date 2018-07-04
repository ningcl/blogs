## S数组冒泡排序

> #### 可以将数组进行排序

代码如下：

~~~
/**
 * 冒泡排序
 * @param array 数组
 * @returns {*}
 */
function maoPaoSort(array){
    var temp;

    for(var i=0;i<array.length;i++){ //比较多少趟，从第一趟开始
        for(var j=0;j<array.length-i-1;j++){ //每一趟比较多少次数
            if(array[j]>array[j+1]){
                temp=array[j];
                array[j]=array[j+1];
                array[j+1]=temp;
            }
        }
    }
    return array;
}

~~~

调用方法：

~~~
var arrry=[85,24,63,17,31,17,86,50];
console.log(maoPaoSort(arrry));
~~~

