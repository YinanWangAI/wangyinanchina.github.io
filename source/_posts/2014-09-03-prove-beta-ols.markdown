---
layout: post
title: "证明多元回归系数的最小二乘性"
date: 2014-09-03 20:42:17 +0800
comments: true
categories:多元回归 证明
description: "统计模型：理论与实践 第四章：多元回归 笔记" 
keywords: 统计模型 多元回归 最小二乘 beta 
---
在多元回归中，我们知道对方程$$Y = X\beta + \epsilon$$中$$$\beta$$$的OLS（通常最小二乘）估计为$$$\widehat{\beta} = (X'X)^{-1}X'Y$$$,下面来证明该性质：

>令$$d(||Y - X\beta||^2) / d\beta = -2\sum_{i=1}^{n}X_i(Y_i - X_i\beta) = 0$$
则$$\beta X'X - X'Y = 0$$
即$$\beta = (X'X)^{-1}X'Y时||Y - X\beta||^2有最小值$$
原式得证。

另一种证明方法是:
>$$||Y - X\beta||^2 = ||Y - X\widehat{\beta} + X\widehat{\beta} - X\beta||^2 = ||Y - X\widehat{\beta}||^2 + ||X\widehat{\beta} - X\beta||^2 + 2||(Y - X\widehat{\beta})'(X\widehat{\beta} - X\beta)||$$ 因为：$$(Y - X\widehat{\beta})'(X\widehat{\beta} - X\beta) = Y'X\widehat{\beta} - YX\beta - \widehat{\beta}'X'X\widehat{\beta} + \widehat{\beta}'X'X\beta = Y'X\widehat{\beta} - YX\beta - Y'X(X'X)^{-1}X'X\widehat{\beta} + Y'X(X'X)^{-1}X'X\beta = 0$$所以当 $$$||X\widehat{\beta} - X\beta||^2$$$最小时$$$||Y - X\beta||^2$$$得到最小值，即$$$\beta = \widehat{\beta}$$$，原式得证。