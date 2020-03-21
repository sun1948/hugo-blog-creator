---
title: "如何用hugo搭建个人博客（for mac）"
date: 2020-03-21T14:38:44+08:00
draft: false
---

总体来说用 hugo 搭建个人博客分为两块：

1. 编辑博客内容，我用的是 vscode
2. 终端生成 public 目录，上传到 github

下面分步骤操作

## 1.安装 hugo

mac 用 homebrew 安装 hugo 很简单，终端运行 `brew install hugo`

运行 `hugo version` ，看到版本号就成功了。

## 2.照着 hugo 官网教程走

进入[hugo 官网](https://gohugo.io/)点击 quick start，按照官网上面的教程，完成 7 步，即可以创建 public 目录，用来上传到 github。

注意:在第 6 步“Site Configuration”时，如果有自己的域名，不想用 github 提供的默认域名，可以修改 baseURL。

## 3.上传 static pages 到 github

为了上传 public 目录，先在 github 上创建一个 repo。

然后在终端里， `cd public` ，接着 git add/ git commit/ git add remote origin git@xxxxxxx /git push，4 连操作上传 public 目录。

## 4.配置 repo 里的 GitHub Pages

完成上传后，打开 github，在对应 repo 里进入 settings，下拉有看到 GitHub Pages，设置 source 为 master branch，页面自动刷新后，再次下拉到 GitHub Pages 处会出现绿色的链接，打开链接即可预览博客

## 其他的

- 可以备份整个博客源代码目录到 github，但要创建.gitignore 文件并添加 public/以忽略它，以免 push 时出错
- 若新增其他博客或者修改之前的博客，操作就简单了，直接运行 hugo 教程里的 Add Some Content，再完成第 5 步和第 7 步，最后在 public 目录下进行 git add、git commit、git push 3 连操作就可以了
- 总之，感觉用 hugo 写博客确实麻烦，可能我是新手白又白，老师也推荐直接知乎、掘金上写博客就好了

The End
