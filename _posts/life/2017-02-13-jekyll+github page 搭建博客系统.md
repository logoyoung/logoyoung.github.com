---
layout: post
comments: true
categories: life
---

### 介绍 
　　相信有很多同学都有写博客记录工作、学习、心情的习惯，
搭建博客网站的途径很多，今天介绍一种利用github page和jekyll
搭建静态博客的方法。当然，这种方式最大的优点就是免费啦。之前写过一个
个人动态网站，需要购买云服务器，安装各种web服务，写脚本语言。
优点是灵活、动态交互。缺点当然是花钱啦。当然，去一些平台写博客
也是不错的，如新浪的SAE，大家可以去试试。

### 工具

* phpStom
* git
* jekyll
* github 账号

### phpStom
　　作为一个php程序员，对于phpStom这款软件有着一定的执着。
写博客用的是markdown语法。markdown语法就不在这里介绍了，点击这里查看[markdown语法](http://www.jianshu.com/p/1e402922ee32/)。发现phpStom这款IDE内置了markdown
语法的预览。因此通过IDE可以边写边预览，也不用麻烦下载其他的预览软件了
，同时在写完代码后不用换软件直接切换到博客环境写总结是不是很爽？

### git
　　上传代码工具


### jekyll
> jekyll是一个简单的免费的Blog生成工具，类似WordPress。但是和WordPress又有很大的不同，
原因是jekyll只是一个生成静态网页的工具，不需要数据库支持。但是可以配合第三方服务,
例如Disqus。最关键的是jekyll可以免费部署在Github上，而且可以绑定自己的域名。


#### 搭建环境
* [安装ruby](http://rubyinstaller.org/downloads/)
　　我的系统是Window，使用RubyInstaller来进行安装。
下载安装完需要将命令添加到系统环境变量里。在命令框中输入ruby -v 检测是否安装成功。
　

* [安装对应的RubyDevKit](http://rubyinstaller.org/downloads/)
>　DevKit是windows平台下编译和使用本地C/C++扩展包的工具。
它就是用来模拟Linux平台下的make,gcc,sh来进行编译。
但是这个方法目前仅支持通过RubyInstaller安装的Ruby

　　打开终端CMD，输入

    ruby dk.rb init
    ruby dk.rb install
    

* 替换rubyGem库地址
　　在国内使用默认的gem源会有问题，需要重新配置gem源。
    
      gem sources --remove https://rubygems.org/
      gem sources -a https://gems.ruby-china.org/
      gem sources -l
    
　　如果遇到 SSL 证书问题，你又无法解决，
请直接用 http://gems.ruby-china.org 避免 SSL 的问题。

   
* 安装rails

　　　　cmd运行`gem install rails`
　　　　cmd运行`rails -v`显示rails版本号说明安装成功.

* 安装Jekyll

```
gem install jekyll
```


### github page
　　注册github账号，创建page仓库这里github网站有介绍，就不进行介绍了。
创建好仓库可以上传自己的代码，同时也可以找jekyll模板。[下载模板](http://jekyllthemes.org/)。
    


### 编写博客

　　我是直接下载的jekyll模板使用，也可以使用jekyll自行创建一个博客项目。
在_post文件下创建mkrkdown文件。  
　　命名为日期加标题如：2017-02-13-jekyll+github page搭建博客系统.md。
编辑如下：

    ---
    layout: post
    comments: true
    categories: life
    ---
    
    ### 介绍 
    　　相信有很多同学都有写博客记录工作、学习、心情的习惯，
    搭建博客网站的途径很多，今天介绍一种利用github page和jekyll
    
　　编写好文件进行编译

    jekyll build
    
　　使用git工具上传到仓库
    
    git add .
    git commit -m "jekyll blog"
    git push
    
　　期间需要输入github账号和密码，输入账号密码就可以上传代码了哦。如果觉得每次输入账号密码[改成ssh方式](http://blog.csdn.net/yuquan0821/article/details/8210944)提交就可以了。去github page网页上看看撰写效果吧。

    


