+++ 
draft = true
date = 2019-09-20T04:17:17-04:00
title = "DP solution of a regex matching problem"
description = "LeetCode No. 10 Regular Expression Matching, DP solution"
slug = "" 
tags = ["leetcode","dp","regex"]
categories = ["leetcode"]
externalLink = ""
series = ["leetcode"]
math = "true"
isCJKLanguage = true
+++

## 题目

<https://leetcode.com/problems/regular-expression-matching/>

## 简单说下DP

> Dynamic programming is both a mathematical optimization method and a computer programming method. The method was developed by Richard Bellman in the 1950s and has found applications in numerous fields, from aerospace engineering to economics. In both contexts it refers to simplifying a complicated problem by breaking it down into simpler sub-problems in a recursive manner. While some decision problems cannot be taken apart this way, decisions that span several points in time do often break apart recursively. Likewise, in computer science, if a problem can be solved optimally by breaking it into sub-problems and then recursively finding the optimal solutions to the sub-problems, then it is said to have optimal substructure.

DP是一种计算机编程方法。但实际上，相比于编程的具体方法而言，它更是一种解决问题的思路。比如相关DP频繁出现的Memoization，top-down approach，bottom-up approach，Recursion等方法，就是基于DP的思路来进行具体编码实现的。

对于DP这种解决问题的思路，最重要的就是找到问题的通用状态。这种状态可以转化到很小以便使问题很容易解决，同时也可以作为更大一层问题解决的依据。这样可以最终转化为解决原问题。

所以对于DP的解决方案，需要着重于找到问题的状态，及状态间的转化。

$$5 + 5$$