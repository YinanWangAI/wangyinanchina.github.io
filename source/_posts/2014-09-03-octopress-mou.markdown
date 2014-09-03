---
layout: post
title: "解决mou中inline公式在octopress中显示混乱的问题"
date: 2014-09-03 22:22:48 +0800
comments: true
categories:
description: "解决mou中inline公式在octopress中显示混乱的问题" 
keywords: mou markdown octopress
---
在mou中行内插入公式使用成对的"$$$"，但是如果使用MathJax的默认配置，将文件上传到octopress中,数学公式并不能很好的显示，<!--more-->解决的方法很简单，将/Users/level5/blog/source/_includes/custom/head.html中的MathJax脚本中

	inlineMath: [ ['$', '$'], ["\\(", "\\)"] ]
	改为inlineMath: [ ['$$$', '$$$'], ["\\(", "\\)"] ]
	
这么做的原因是MathJax默认的插入行内公式是"$"，而mou是"$$$"，所以我们需要把"$"改为"$$$"。
	