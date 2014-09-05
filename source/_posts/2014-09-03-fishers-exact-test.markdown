---
layout: post
title: "超几何分布和fisher精确检验"
date: 2014-09-03 23:30:07 +0800
comments: true
categories: 假设检验
description: "解决mou中inline公式在octopress中显示混乱的问题" 
keywords: 超几何分布 fisher's test 假设检验
---
Fisher精确检验(fisher's exat test)是进行统计分析时经常碰到的一种检验方法，它基于超几何分布，作用于离散变量，用于检测两种分类方法的结果是否独立。

首先，我们介绍超几何分布。超几何分布用来模拟这样的过程：将有限的总体分为两类A和B，从中不放回的抽样n次，结果中A的个数符合超几何分布。所以使用古典概型的方法，假设N个总体中有A和B两类，其中A有K个，从中不放回的抽样n次，我们可以推导出n中为A的数目x，即超几何分布的pmf:$$P(X = x) = \binom{K}{x} \binom{N - K}{n - x} / \binom{N}{n}$$

回到fisher精确检验，fisher检验要回答的问题是，对数据进行两种分类，这两种分类是否独立？即在第一种分类条件下分为某一类的数据是否更倾向于在第二种分类中归于某类。举例说明\([例子来源于wiki](http://en.wikipedia.org/wiki/Fisher's_exact_test)\)：
>我们有24位测试对象，根据其性别和是否患有糖尿病，将其分为四类，分类结果如下：

$$
\begin{matrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{matrix}
$$