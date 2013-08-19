---
title : Ready for GO ?
layout: post
categories : ["Let's GO!"]
tagline: ""
tags : ["GO","转载学习"]
published: true
---
{% include JB/setup %}
    这篇文章作为Markdown编写练习吧~ 顺便学学GO语言。

>转自：<http://www.shenyisyn.org/2013/06/09/golang-1.htm>

##GO语言介绍
1. GO语言的东家是Google，这个重磅级的名字足可以让你至少停下来关注一番。
2. 理论上大部分C能干到的事情GO大部分也能干到。
3. 在Linux、windows各个方面支持的都很好。
4. 个人认为Android将来肯定会被Google用GO语言代替。
5. GO语言的语法简化很有理由，严谨中透出一种自由的感觉。自由实际上是程序员最梦想要得到却很难得到的东西。
6. 为什么GOOGle能成功，其良好的用户体验是很大一部分原因；而GO语言框架也让程序员在使用时带来了强大“程序员体验”—不信大家可以试试。
7. Go语言在什么地方应用？这个还没有定论，至少我们项目中打算在电商后台的统计、分析、数据挖掘上使用GO语言做替代版本。至于说有人问GO语言是否能做网页？我觉得连word都能做网页，这完全是两回事。

这里我申明一下，因为目前还处在学习阶段，所以我使用的是windows部署对应的环境，用记事本作为开发环境。

注意：正式的项目开发，应该移植到linux平台。开发环境应该使用智能编辑器，不要使用记事本，除非你的时间实在很多，也不缺钱花，女朋友也不缺，累了也不怎么看苍老师。


##部署
###一、首先要到Google去下载对应的编译器。
>地址如下：   <https://code.google.com/p/go/downloads/list>

1. 这里我建议大家下载： go1.1.windows-386.zip  不要下载安装版，手动配置一下,很方便。
2. 解压缩后，把文件夹重新命名为 go—原因很简单，简单点方便看的爽。我是放在 E:/go这个文件夹中的
3. 添加用户变量和系统变量。其中用户变量，添加变量名“GOROOT” ，变量值”E:/go”。

系统变量在“Path”变量中加入”E:/go/bin”  .系统变量使用“;”即英文分号分隔的哦

以上就好了，多方便。一点不拖泥带水，不要你重启、不要你看广告、不要你把某浏览器设置为默认浏览器、不要你填写调查问卷、不要你同意狗屁协议、不要你把苍老师的视频删掉腾出空间给它(大家想想vs.net一条龙文件吧)



###二、写一段GO语言程序
在E:/go/bin  下面建立一个txt文件夹叫 test.go

输入代码
{% highlight go %}
package main
import "fmt" //fmt包含有格式化I/O函数，类似于C语言的printf和scanf。格式字符串的规则来源于C但更简单一些。
func main() {  //这个大括号一定要在这里，不能空行
 fmt.Printf("失业的程序员!")  //记住不要分号
}
{% endhighlight %}

好了保存。

###三、运行刚才的测试程序
打开”cmd”窗口

{% highlight bash %}
cd E:/go/bin   //这一切是为了调用 这个文件夹里面的 go.exe 来编译 刚才写的 test.go
{% endhighlight %}

执行以下语句
{% highlight bash %}
go build test.go
{% endhighlight %}

1. go  代表 bin文件夹下有个  exe叫做go
2. build 是参数，代表是编译
3. test.go 是要编译的文件名。当然你可以把这个文件放在 c:/test.go
4. 后面还有参数，不过这里省略了。这样自动会在 E:/go/bin 下面生成一个 test.exe 可执行文件。如果是go build test.go c:/test.ext   那么会在c盘下生成。
5. 直接在 cmd下面运行 test.exe，则会输出“失业的程序员”这个字符串。

>Over