# GDbox概述
## 背景
- GDBox(Game Design Box)是一个Excel的插件，大约自2013年的时候利用个人业余时间开发至今。从名字可以看出来是和游戏策划工作相关的一个插件工具。在经历了多个上线项目之后沉淀了一些功能。希望能够让更多的人用到这款工具。
- 作为一介策划，代码写的很垃圾，可能有很多Bug还望包涵。有任何问题可以邮件或者反馈Issues。

# 安装与使用
## 必备组件
- 你需要有Office 365或者Office 2010并安装了Excel。
- 目标框架为.Net Framework 4.0 Client Profile，一般都会有、没有的话可能要去下载一个。

## 安装
- 解压缩安装包，运行setup.exe即可。
- 打开Excel就能够看到新得插件页。

## 卸载
- 在Windows的应用程序管理里找到GDbox即可进行卸载。

# 核心功能介绍
## XML的导出功能
- 可以将Excel导出成各种形式不同的Xml，以适配项目组开发的读取需求，使得在开发不支持Excel的情况下策划依然可以使用Excel作为数据编辑环境。

## [暂时关闭]分支管理功能
- 许多项目会用到许多分支，然后会导致策划需要在各个分支间重复配置。其间会发生大量的同步的错误（如数据结构不一致带来的复制错误）。这个分支管理功能的核心述求是通过同一份Excel来导出行列各不相同的Excel或者Xml等。
- 当前的实现有许多固化的功能，此部分将在配置化后再次开放。

## 数据结构自动化代码
- Excel定义数据结构与生成相应的反序列化代码的功能。
- 基本操作流程是先创建一个数据模板，然后使用这个模板可以同时生成Excel表格供策划使用及相关的代码给开发使用。

## 数据连接
- 在Excel表格配置工作中，许多时候会有需要配置ID的工作；而配置ID是一个低效且容易出错的过程。通过数据连接，可以关联某一个字段到另外一张工作簿或者工作页的ID，通过显示ID对应的注释、名称的形式来实现通过点选（支持搜索）的形式来进行ID的配置。
- 快速创建是实现数据连接最简单的方式，数据连接窗口则可以进行统一的管理。

## 数据描述与自动化编辑器
- 数据结构除了使用Excel定义之外，更推荐的是使用GDE编辑器（GDE编辑器的【编辑】）来创建。
- GDBox会为每一个Excel创建一个对应名称的GDE文件（本质为Xml）来描述这个Excel的数据结构；而GDE编辑器则是用来对这个数据描述进行编辑的。
- 通过GDE编辑器，可以解锁更多的自动化的功能，比如让数据连接支持多选、枚举字段变成下拉框选择等功能。
- 在有了GDE文件之后，就可以生成自动的数据编辑器，点击（GDE编辑器的【打开】）即可，编辑器将自动根据GDE的配置来生成，主要用于关联性内容的点选性编辑。这个编辑器使得Excel的数据编辑多了一种可能。

## 控制台与差异比较工具
- 控制台主要用于工具本身的日志显示与错误调试。将来也许会引入更多的指令支持指令化的Excel内容编辑。
- 差异比较工具可以比较两个Excel的差异，并选择哪一个单元格需要Merge到最终的Excel。在差异化可视性方面并没有BeyondCompare好，优势就是在于可以方便修改差异。
- 如果没有正版BeyondCompare可以勉为其难用用这个。

# 更新日志
## 0.6.6.46
- 去除了和项目中相关的功能
- 暂时屏蔽了分支管理导出功能。
- 修复了部分由于Excel数据为空导致的Bug。

## 0.6.6.47
- 添加了【本地化文本】的新字段类型
- 添加了Excel对于本地化文本的支持，现在可以在Excel中直接编辑使用Key索引的本地化文本了
