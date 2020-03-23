---
title: "HTML常用标签"
date: 2020-03-23T10:02:22+08:00
draft: false
---
## 一、a 标签的用法
a标签功能蛮强大的，主要依托href/target属性实现，其中href有4类取值，target有5种取值。

另外download的作用不是打开页面而是下载页面，问题在于不是所有浏览器都支持（尤其手机）；rel=noopener我暂时不清楚。
#### href属性
1. 跳转到外部页面
   href=" ",可以填
   * 网址：不用写完整，直接//google.com即可
   * 其他页面：绝对/相对路径均可。注意：根目录/表示http-sever建立的目录。
2. 跳转到内部锚点
   * href="#",跳转到页面顶部
   * href="#xxx",调转到id=xxx的元素
3. 跳转到电话、邮件
   * href="mailto:xxx@xxx.com",跳转$$到邮箱
   * href="tel:xxxxxxx",跳转到电话
4. 伪协议
   * href="javascript:xxx;"，当xxx为空时，可以实现点击a标签啥都不干
#### target属性
页面跳转的目标，4+1，内置+程序员命名
1. 默认_self 当前页面下跳转
2. _blank 跳转到空白页面
3. _top 最上层页面下跳转
4. _parent 父级页面下跳转
5. window的name，iframe的name
## 二、img 标签的用法
作用：是发送get请求展示图片

属性如下：
1. src="图片路径" 绝对/相对路径均可
2. width、height 设置宽高（此处不用加单位px），设置一个另一个会自适应；
   在css中设置max-width：100%，可实现响应式布局
3. alt=“xxx”，可替代的，图片加载失败后的描述

事件：onload、onerror，失败时可以展示图片
## 三、table 标签的用法
作用：绘制表格
样式：table-layout: fixed/auto,均匀分布/根据内容调整；

border-collapse: collapse，border-spacing: 0, 二者实现表格内部间隙0，初始化会使用

相关标签：thead\tbody\tfoot,tr\th\td
## 其他感想
html的重要标签很多，表单form、输入类标签input、select+option、textarea、label、音视频标签video、audio、canvas、svg(兼容性要查文档)
### form 标签
作用：发送GET/POST请求，刷新页面

属性：
* action=“请求页面的地址”
* method=“GET/POST”
* autocomplete实现input等表单自动填充
* target和在a标签里面用法一致。

事件: onsubmit

注意：
* form里面的input必须有“name”属性，否则影响后续提交
* 必须有一个type类型是submit的标签（input/button）
### input 标签
作用：通过type属性实现各种输入，文本、密码、提交、原点、上传文件、颜色等

属性：
* type，取值有：text、password、submit、radio、checkbox、file（+multiple）、color等
* 其他属性：name等等
* html5增强功能：required 必须输入内容，不输入会提示

事件：onfocus\onblur\onchange


## The End