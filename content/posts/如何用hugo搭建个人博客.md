---
title: "如何用hugo搭建个人博客（for mac）"
date: 2020-03-21T14:38:44+08:00
draft: false
---

总体来说用hugo搭建个人博客分为两块：
1. 编辑博客内容，我用的是vscode
2. 终端生成public目录，上传到github
   
下面分步骤操作
# 1.安装hugo
mac用homebrew安装hugo很简单，终端运行 `brew install hugo`

运行 `hugo version` ，看到版本号就成功了。
# 2.打开[hugo官网](https://gohugo.io/)，照着教程走
点击quick start，按照官网上面的教程，完成7步，即可以创建public目录，用来上传到github。

注意:在第6步“Site Configuration”时，如果有自己的域名，不想用github提供的默认域名，可以修改baseURL。
# 3.上传static pages到github
为了上传public目录，先在github上创建一个repo。

然后在终端里， `cd public` ，接着git add/ git commit/ git add remote origin git@xxxxxxx /git push，4连操作上传public目录。
# 4.配置repo里的GitHub Pages
完成上传后，打开github，在对应repo里进入settings，下拉有看到GitHub Pages，设置source为master branch，页面自动刷新后，再次下拉到GitHub Pages处会出现类似链接：

![](../../public/images/截屏2020-03-21下午4.40.52.png)

打开链接，即可预览博客

其他的
* 可以备份整个博客源代码目录到github，但要创建.gitignore文件并添加public/以忽略它，以免push时出错
* 若新增其他博客或者修改之前的博客，操作就简单了，直接运行hugo教程里的Add Some Content，再完成第5步和第7步，最后在public目录下进行git add、git commit、git push 3连操作就可以了
* 总之，感觉用hugo写博客确实麻烦，可能我是新手白又白，老师也推荐直接知乎、掘金上写博客就好了

  
  
The End