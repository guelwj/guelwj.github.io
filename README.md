# Gue君爷的日常note

>记录平时项目中遇到问题时的解决方案，附上能找到答案的网址、分享一些不错的资源。

## 目录：
1. [分享一个不错的git教学视频](#分享一个不错的git教学视频)
2. [微信公众平台文档](#微信公众平台文档)
3. [大白话讲解Promise](#大白话讲解Promise)
4. [前端布局神器flex](#前端布局神器flex)
5. [js模块化编程之彻底弄懂CommonJS和AMD/CMD](#js模块化编程之彻底弄懂CommonJS和AMD/CMD)
6. [git_push错误failed_to_push_some_refs_to](#git_push错误failed_to_push_some_refs_to)
7. [使用Flexible实现手淘H5页面的终端适配](#使用Flexible实现手淘H5页面的终端适配)
8. [入门Webpack，看这篇就够了](#入门Webpack，看这篇就够了)
9. [video搭配canvas的神奇效果](#video搭配canvas的神奇效果)
10. [video在安卓大部分浏览器包括微信最顶层的问题](#video在安卓大部分浏览器包括微信最顶层的问题)
11. [js控制输入框光标位置（setSelectionRange详解）](#js控制输入框光标位置（setSelectionRange详解）)
12. [jquery中attr和prop的区别介绍](#jquery中attr和prop的区别介绍)
13. [拖放排序插件Sortable.js](#拖放排序插件Sortable.js)
14. [ios与android差异，new_Date()之坑](#ios与android差异，new_Date()之坑)
15. [原生js实现瀑布流效果](#原生js实现瀑布流效果)
16. [微信小程序RSA签名验签加密解密](#微信小程序RSA签名验签加密解密)
17. [解决VS2017隐藏“高级保存选项”命令](#解决VS2017隐藏“高级保存选项”命令)
18. [airbnb/javascript标准](#airbnb/javascript标准)


## 分享一个不错的git教学视频
git权威指南教程：http://www.icoolxue.com/album/show/41


## 微信公众平台文档
https://developers.weixin.qq.com/miniprogram/dev/


## 大白话讲解Promise
https://www.cnblogs.com/lvdabao/p/es6-promise-1.html


## 前端布局神器flex
https://www.cnblogs.com/qingchunshiguang/p/8011103.html


## js模块化编程之彻底弄懂CommonJS和AMD/CMD
https://www.cnblogs.com/chenguangliang/p/5856701.html


## git_push错误failed_to_push_some_refs_to
解决方案：
在github库中对某个文件进行了在线的编辑，并且没有同步到本地库，之后我在本地库添加了文件test.txt，并想提交到github，出现以下错误：error：failed to push some refs to。
这个问题是因为远程库与本地库不一致造成的，那么我们把远程库同步到本地库就可以了。 
使用指令 git pull --rebase origin master
这条指令的意思是把远程库中的更新合并到本地库中，--rebase的作用是取消掉本地库中刚刚的commit，并把他们接到更新后的版本库之中。

https://blog.csdn.net/mbuger/article/details/70197532


## 使用Flexible实现手淘H5页面的终端适配
https://github.com/amfe/article/issues/17?utm_source=caibaojian.com


## 入门Webpack，看这篇就够了
https://www.jianshu.com/p/42e11515c10f


## video搭配canvas的神奇效果
http://html5doctor.com/video-canvas-magic/


## video在安卓大部分浏览器包括微信最顶层的问题
解决不了。
https://segmentfault.com/q/1010000004436205/a-1020000004436328


## js控制输入框光标位置（setSelectionRange详解）

解决方案：
```javascript
var inpObj = document.getElementById(inputId);
if (inpObj.setSelectionRange) {
    inpObj.setSelectionRange(0, inpObj.value.length);
}
```

https://blog.csdn.net/foralienzhou/article/details/52437929


## jquery中attr和prop的区别介绍

对于HTML元素本身就带有的固有属性，在处理时，使用prop方法。
对于HTML元素我们自己自定义的DOM属性，在处理时，使用attr方法。

https://www.jb51.net/article/88068.htm


## 拖放排序插件Sortable.js
https://segmentfault.com/a/1190000008209715


## ios与android差异，new_Date()之坑

例如：
var date = '2016-02-28 16:42:54.0';

android:
new Date(date)
//Sun Feb 28 2016 16:42:54 GMT+0800 (中国标准时间)

ios:
new Date(date)
//Invalid Date = $1     不能将含有'－'的时间字符串转成时间。
//Invalid Date = $2     '.0'表示的毫秒不能转
new Date(date.replace(/\-/g,'/').replace('.0',''));
//The Feb 18 2016 16:42:54 GMT+0800 (CST)

http://www.mamicode.com/info-detail-1392511.html


## 原生js实现瀑布流效果
https://segmentfault.com/a/1190000012621936


## 微信小程序RSA签名验签加密解密
https://github.com/zhangzhaopds/WeixinApp_RSA_Signature


## 解决VS2017隐藏“高级保存选项”命令
（1）单击“工具”|“自定义”命令，弹出“自定义”对话框。
（2）单击“命令”标签，进入“命令”选项卡。
（3）在“菜单栏”下拉列表中，选择“文件”选项。
（4）单击“添加命令”按钮，弹出“添加命令”对话框。
（5）在“类别”列表中，选择“文件”选项；在“命令”列表中，选择“高级保存选项”选项。
（6）单击“确定”按钮，关闭“添加命令”对话框。
（7）选中“控件”列表中的“高级保存选项”选项，单击“上移”或者“下移”按钮，调整该命令的位置。
（8）单击“关闭”按钮，完成“高级保存选项”命令的添加操作。


## airbnb/javascript标准
https://github.com/airbnb/javascript#table-of-contents