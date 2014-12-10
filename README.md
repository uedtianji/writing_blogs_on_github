#如何使用Github pages写博客  

**为什么要用Github搭建博客？**  

**免费**，虽然csdn、cnblog也是免费的，但是那种只提供在线编辑，不能随意修改页面样式的网站当然没法满足我们这种折腾惯了的个人站长。用wordpress自己搭建网站，租用服务器也是一笔费用。而github可以随意定制、指定自己的域名，完全满足个人站长的需求，关键是完全免费。  

**Markdown**便捷的文章书写体验,虽然 zblog、wordpress安装插件也可以支持markdown语法，但是github的README.md一直使用markdown语法直接显示在项目的页面中，使用markdown的支持更方便。  

**Github pages 无法实现什么功能？**  

文章评论，github pages只支持静态页面的展示，虽然浏览器端可以使用javascript控制逻辑，但是缺少服务器端语言的支持，所以无法处理提交的评论。好在我们可以使用第三方的评论插件，如[多说](http://duoshuo.com/)、[友言](http://www.uyan.cc/)等。这些第三方评论插件将评论上传到他们的服务器上，这样便于管理还可以使用他们的垃圾评论过滤器，更加的方便、安全。  

####步骤  

1. 新建repository   
这里要注意项目名称。如果项目名称是```username.github.com```或```username.github.io```,其中```username```为你的github名称或者组织名称，则生成的github pages是```个人主页```。如果项目名称为其他名称则是```项目主页```。  
个人主页和项目主页的区别:    
>个人主页的页面文件存放在```master```分支下
>项目主页的页面文件存放在```gh-pages```分支下

2. 如果是**项目主页**，在项目目录中进入```Settings```  
![](https://raw.githubusercontent.com/uedtianji/writing_blogs_on_github/master/images/1.jpg)  
在settings中的```Github pages```点击```Automatic page generator```进入页面编辑。  
![](https://raw.githubusercontent.com/uedtianji/writing_blogs_on_github/master/images/2.jpg)  
在页面编辑中建议使用```Load README.md```来将README.md中的内容加载到页面中。  
![](https://raw.githubusercontent.com/uedtianji/writing_blogs_on_github/master/images/3.jpg)  
选择模版样式后，github将建好```gh-pages```分支。  
![](https://raw.githubusercontent.com/uedtianji/writing_blogs_on_github/master/images/4.jpg) 

3.如果是**个人主页**，则不需要进入```Settings```，github将会在```master```分支中建好页面静态文件。  

4.访问```http://username.github.io```(个人主页)或者```http://username.github.io/项目名称```(项目主页)就可以访问页面了。  

5.修改页面。修改```master```(个人主页)或者```gh-pages```(项目主页)中的html文件就可以修改页面内容了，页面中的路径使用的相对路径，相对的目录是项目根目录。  

6.github默认用来生成静态文件的工具是```jekyll```,jekyll是用Ruby编写，用不惯的可以尝试下使用我自己编写的```githubpress```使用nodejs编写。

7.绑定域名。在```master```(个人主页)或者```gh-pages```(项目主页)版本库下新建名字为CNAME的文本文件，注意无扩展名,内容为域名，如：ued.sexy。然后在你的域名提供商那里添加A记录或者cname到github的ip```192.30.252.153```、```192.30.252.154```,然后等待生效就可以用你自己的域名访问了。







