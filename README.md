# firstGroup 
## 常用命令
- git branch 查看本地所有分支
- git status 查看当前状态 
- git commit 提交 
- git branch -a 查看所有的分支
- git branch -r 查看远程所有分支
- git commit -am "init" 提交并且加注释 
- git remote add origin git@192.168.1.119:ndshow
- git push origin master 将文件给推到服务器上 
- git remote show origin 显示远程库origin里的资源 
- git push origin master:develop
- git push origin master:hb-dev 将本地库与服务器上的库进行关联 
- git checkout --track origin/dev 切换到远程dev分支
- git branch -D master develop 删除本地库develop
- git checkout -b dev 建立一个新的本地分支dev
- git merge origin/dev 将分支dev与当前分支进行合并
- git checkout dev 切换到本地dev分支
- git remote show 查看远程库
- git add .
- git rm 文件名(包括路径) 从git中删除指定文件
- git clone git://github.com/schacon/grit.git 从服务器上将代码给拉下来
- git config --list 看所有用户
- git ls-files 看已经被提交的
- git rm [file name] 删除一个文件
- git commit -a 提交当前repos的所有的改变
- git add [file name] 添加一个文件到git index
- git commit -v 当你用－v参数的时候可以看commit的差异
- git commit -m "This is the message describing the commit" 添加commit信息
- git commit -a -a是代表add，把所有的change加到git index里然后再commit
- git commit -a -v 一般提交命令
- git log 看你commit的日志
- git diff 查看尚未暂存的更新
- git rm a.a 移除文件(从暂存区和工作区中删除)
- git rm --cached a.a 移除文件(只从暂存区中删除)
- git commit -m "remove" 移除文件(从Git中删除)
- git rm -f a.a 强行移除修改后文件(从暂存区和工作区中删除)
- git diff --cached 或 $ git diff --staged 查看尚未提交的更新
- git stash push 将文件给push到一个临时空间中
- git stash pop 将文件从临时空间pop下来
- ---------------------------------------------------------
- git remote add origin git@github.com:username/Hello-World.git
- git push origin master 将本地项目给提交到服务器中
- -----------------------------------------------------------
- git pull 本地与服务器端同步
- -----------------------------------------------------------------
- git push (远程仓库名) (分支名) 将本地分支推送到服务器上去。
- git push origin serverfix:awesomebranch
- ------------------------------------------------------------------
- git fetch 相当于是从远程获取最新版本到本地，不会自动merge
- git commit -a -m "log_message" (-a是提交所有改动，-m是加入log信息) 本地修改同步至服务器端 ：
- git branch branch_0.1 master 从主分支master创建branch_0.1分支
- git branch -m branch_0.1 branch_1.0 将branch_0.1重命名为branch_1.0
- git checkout branch_1.0/master 切换到branch_1.0/master分支
- du -hs
- 
- git branch 删除远程branch
- git push origin :branch_remote_name
- git branch -r -d branch_remote_name
- ------------------------------------------------------------
- 
- 初始化版本库，并提交到远程服务器端
- mkdir WebApp
- cd WebApp
- git init 本地初始化
- touch README
- git add README 添加文件
- git commit -m 'first commit'
- git remote add origin git@github.com:daixu/WebApp.git

- 增加一个远程服务器端

- 上面的命令会增加URL地址为'git@github.com:daixu/WebApp.git'，名称为origin的远程服务器库，以后提交代码的时候只需要使用 origin别名即可
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
## 更短的数组去重写法
```
[...new Set([2,"12",2,12,1,2,1,6,12,13,6])]

// [2, "12", 12, 1, 6, 13]
```
## 排序算法
```
升序：
var numberArray = [3,6,2,4,1,5];
numberArray.sort(function(a,b){  
   return a-b;
})
console.log(numberArray);
```

## 冒泡排序
```
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
```
### null和undefined的区别：
- null：表示无值；undefined：表示一个未声明的变量，或已声明但没有赋值的变量，
- 或一个并不存在的对象属性。

### 使用闭包的注意点：
- 由于闭包会使得函数中的变量都被保存在内存中，内存消耗很大，所以不能滥用闭包，否则会造成网页的性能问题，在IE中可能导致内存泄露。解决方法是，在退出函数之前，将不使用的局部变量全部删除。

- 闭包会在父函数外部，改变父函数内部变量的值。所以，如果你把父函数当作对象（object）使用，把闭包当作它的公用方法（Public Method），把内部变量当作它的私有属性（private value），这时一定要小心，不要随便改变父函数内部变量的值。 
（关于闭包，详细了解请看JavaScript之作用域与闭包详解）
## 请解释JSONP的工作原理，以及它为什么不是真正的AJAX。
- JSONP (JSON with Padding)是一个简单高效的跨域方式，HTML中的script标签可以加载并执行其他域的javascript，于是我们可以通过script标记来动态加载其他域的资源。例如我要从域A的页面pageA加载域B的数据，那么在域B的页面pageB中我以JavaScript的形式声明pageA需要的数据，然后在 pageA中用script标签把pageB加载进来，那么pageB中的脚本就会得以执行。JSONP在此基础上加入了回调函数，pageB加载完之后会执行pageA中定义的函数，所需要的数据会以参数的形式传递给该函数。JSONP易于实现，但是也会存在一些安全隐患，如果第三方的脚本随意地执行，那么它就可以篡改页面内容，截获敏感数据。但是在受信任的双方传递数据，JSONP是非常合适的选择。

- AJAX是不跨域的，而JSONP是一个是跨域的，还有就是二者接收参数形式不一样！

## 请解释变量声明提升。
- 在函数执行时，把变量的声明提升到了函数顶部，而其值定义依然在原来位置。

## 28.如何从浏览器的URL中获取查询字符串参数。
- 以下函数把获取一个key的参数。
```
  function parseQueryString ( name ){
      name = name.replace(/[\[]/,"\\\[");
      var regexS = "[\\?&]"+name+"=([^&#]*)";
      var regex = new RegExp( regexS );
      var results = regex.exec( window.location.href );
 
      if(results == null) {
          return "";
      } else {
     return results[1];
     }
 }
 ```
## arguments是什么？
- arguments虽然有一些数组的性质，但其并非真正的数组，只是一个类数组对象。
- 其并没有数组的很多方法，不能像真正的数组那样调用.jion(),.concat(),.pop()等方法。

## 什么是”use strict”;?使用它的好处和坏处分别是什么？
- 在代码中出现表达式-“use strict”; 意味着代码按照严格模式解析，这种模式使得Javascript在更严格的条件下运行。

- 好处：
 - 1.消除Javascript语法的一些不合理、不严谨之处，减少一些怪异行为;
 - 2.消除代码运行的一些不安全之处，保证代码运行的安全；
 - 3.提高编译器效率，增加运行速度；

- 坏处：
 - 1.同样的代码，在”严格模式”中，可能会有不一样的运行结果；一些在”正常模式”下可以运行的语句，在”严格模式”下将不能运行。
