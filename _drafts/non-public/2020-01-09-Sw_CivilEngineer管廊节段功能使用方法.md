---
layout: post
category: Sw_CivilEngineer
title: Sw_CivilEngineer管廊节段功能使用方法
tagline: by 明不知昔
tags: 
  - ORD
  - BIM
  - Sw_CivilEngineer
published: true
---

<!--more-->

# 功能简介

## 位置

sw_CivilEnginneer > sw_Concrete > 桥隧管廊 > 管廊节段

## 功能介绍

[管廊节段] 功能是在 Default 中沿着一条中心线放置参数化的截面。

# 使用环境

1. 工作空间：sw_Structure
2. 工作 Model: Default
3. 中心线要求：需使用道路中线工具绘制中心线分别进行平面和纵段面设计
4. 需要有参数化截面

# 参数说明

![管廊节段功能界面.png](https://i.loli.net/2020/01/09/yJiplxK1eE95dLF.png)

| 名称     | 描述                                 |
| -------- | ------------------------------ |
| 类型     | 选择参数化截面                       |
| 起始里程 | 选择中心线的起始点的里程。格式：Km+m |
| 布置间距 | 格式：节段数\*单个节段长              |
| 沉降缝   | 沉降缝宽度                           |
| 横向偏移 | 参数化截面定义的原点横向偏移中心线的距离，沿路线前进方向：左负右正 |
| 沉降缝   | 参数化截面定义的原点竖向偏移中心线的距离。下负上正 |
| 更新模型 | 勾选：在原来模型的基础上更新；不勾选：保留原来的模型，生成新的模型 |



# 参数化截面定义规则

1. Dgn 文件命名为：sw_ParametricStructure.cel
2. 包含参数化截面的 Model 命名：以 ”管廊节段_“ 开头，例如：”管廊节段\_单舱“
3. 参数化截面定义平面：在 YZ 平台定义，X正方向默认为前进方向
4. 截面定位点位于世界坐标系的原点

# 使用步骤

1. 激活功能
2. 根据提示，选择中心线
3. 选择节段类型
4. 如果类型中没有自己需要的类型，则新建截面单元库，命名为：sw_ParametricStructure.cel，然后将该文件拷贝到路径：`工作集路径\Standards\Cell`目录里面，然后再激活功能
5. 输入相关参数
6. 左键开始生成