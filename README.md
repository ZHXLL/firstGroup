# firstGroup 
## 如何阻止事件冒泡和默认事件
- stoppropagation / preventdefault

## 添加 插入 替换 删除到某个接点的方法
- obj.appendChidl()
- obj.innersetBefore
- obj.replaceChild
- obj.removeChild

## 解释jsonp的原理，以及为什么不是真正的ajax
- 动态创建script标签，回调函数
- Ajax是页面无刷新请求数据操作

## javascript的本地对象，内置对象和宿主对象
- 本地对象为array obj regexp等可以new实例化
- 内置对象为gload Math 等不可以实例化的
- 宿主为浏览器自带的document,window 等

## document load 和document ready的区别
- 页面加载完成有两种事件：
 - 一.是ready，表示文档结构已经加载完成（不包含图片等非文字媒体文件）。
 - 二.是onload，指示页面包含图片等文件在内的所有元素都加载完成。

## ”==”和“===”的不同
- 前者会自动转换类型
- 后者不会

## javascript的同源策略
- 同源策略是一个很重要的安全理念，它在保证数据的安全性方面有着重要的意义，
- 一段脚本只能读取来自于同一来源的窗口和文档的属性，这里的同一来源指的是协议、域名和端口号的组合

## 最快捷的数组求最大值
```
var arr = [ 1,5,1,7,5,9];
Math.max(...arr)  // 9 
```
21.更短的数组去重写法
- [...new Set([2,"12",2,12,1,2,1,6,12,13,6])]

// [2, "12", 12, 1, 6, 13]
22.排序算法
升序：

var numberArray = [3,6,2,4,1,5];
numberArray.sort(function(a,b){  
   return a-b;
})
console.log(numberArray);
23.冒泡排序
var examplearr=[8,94,15,88,55,76,21,39];
function sortarr(arr){
    for(i=0;i<arr.length-1;i++){
        for(j=0;j<arr.length-1-i;j++){
            if(arr[j]>arr[j+1]){
                var temp=arr[j];
                arr[j]=arr[j+1];
                arr[j+1]=temp;
            }
        }
    }
    return arr;
}
sortarr(examplearr);
console.log(examplearr);
24.null和undefined的区别：
null：表示无值；undefined：表示一个未声明的变量，或已声明但没有赋值的变量，
或一个并不存在的对象属性。

25.使用闭包的注意点：
1.由于闭包会使得函数中的变量都被保存在内存中，内存消耗很大，所以不能滥用闭包，否则会造成网页的性能问题，在IE中可能导致内存泄露。解决方法是，在退出函数之前，将不使用的局部变量全部删除。

2.闭包会在父函数外部，改变父函数内部变量的值。所以，如果你把父函数当作对象（object）使用，把闭包当作它的公用方法（Public Method），把内部变量当作它的私有属性（private value），这时一定要小心，不要随便改变父函数内部变量的值。 
（关于闭包，详细了解请看JavaScript之作用域与闭包详解）
