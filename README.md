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

2. 在项目目录中进入```Settings```  
![](https://raw.githubusercontent.com/uedtianji/writing_blogs_on_github/master/images/1.jpg)  
在settings中的```Github pages```点击```Automatic page generator```进入页面编辑。  
![](https://raw.githubusercontent.com/uedtianji/writing_blogs_on_github/master/images/2.jpg)  
在页面编辑中建议使用```Load README.md```来将README.md中的内容加载到页面中。  
![](https://raw.githubusercontent.com/uedtianji/writing_blogs_on_github/master/images/3.jpg)  
选择模版样式后完毕。  







