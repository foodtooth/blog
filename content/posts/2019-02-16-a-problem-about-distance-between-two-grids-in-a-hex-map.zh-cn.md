+++ 
draft = false
date = 2019-09-20T05:02:58-04:00
title = "A problem about distance between two grids in a hex map"
description = ""
slug = "" 
tags = ["hexagon","hex map"]
categories = []
externalLink = ""
series = []
isCJKLanguage = true
+++

## 题目是
如下图所示的Hex map中

![Problem description](https://i.imgur.com/IG2lwOG.jpg)

求任意两个数字的grid之间的最短距离

## 读题意
题中Hex map的特点是

1. 格中数字呈spiral ring方式递增
2. grid放置呈flat形式

Hex map本身特点有

1. 到所有相邻grid距离相等

## 思路是
利用Hex map的坐标系统。但是题中数字不是坐标系统的规律，所以要在进行对应后，再使用坐标系统的规范方法

1. 坐标系统选用Cube coordinates，便于理解
2. 距离计算选用适用其变种的Axial coordinates的方式
3. 此坐标系下

> distance is derived from the Mahattan distance on cubes

## Code
<iframe height="400px" width="100%" src="https://repl.it/@foodtooth/LightyellowHumbleDisassembler?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

With some memos:

![Simple memo](https://i.imgur.com/8kQN0AA.jpg)