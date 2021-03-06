---
title: 什么是游标？  （访问桌面数据库参考 （英文）
TOCTitle: What is a Cursor?
ms:assetid: cc70d941-05e0-9b14-1c5d-6b1a5802f546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250013(v=office.15)
ms:contentKeyID: 48547738
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0bedbeb041d919cd417ade215ac71b9eabbc4de2
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947593"
---
# <a name="what-is-a-cursor"></a>什么是游标？


**适用于**： Access 2013、 Office 2013

游标是关系数据库中作用于完整行集的操作。SELECT 语句返回的行集由满足该语句中 WHERE 子句条件的所有行组成。该语句返回的完整行集称为结果集。应用程序（特别是那些处于交互和联机模式的应用程序）不能总是有效地将整个结果集作为一个整体来处理。这些应用程序需要一个机制，以便一次处理一行或一小块行。游标是提供该机制的结果集的扩展。

游标由游标库实现。游标库是一个软件，通常作为数据库系统的一部分或数据访问 API 来实现，用于管理从数据源（结果集）所返回数据的属性。这些属性包括并发管理、结果集内的位置、返回的行数以及是否可以在结果集中向前/向后移动（可滚动性）。

游标可跟踪结果集内的位置，并允许您针对结果集逐行执行多种操作，可以返回初始表也可以不返回到初始表。换言之，在概念上，游标基于数据库中的表返回结果集。之所以这样命名，是因为游标指示结果集内的当前位置，正如计算机屏幕上的光标指示当前位置一样。

一定要先熟悉游标的概念，然后再接着了解有关它们在 ADO 中用法的详细说明。

使用游标，您可以执行下列操作：

  - 指定特定行在结果集内的位置。

  - 基于结果集内的当前位置来检索一行或一个行块。

  - 修改位于结果集内当前位置的行中的数据。

  - 定义对其他用户所做的数据更改的不同敏感度级别。

例如，假设有一个向潜在购买者显示可用产品列表的应用程序。购买者浏览该列表，查看产品的详细信息和价格，并最终选择要购买的产品。对于该列表中的其余部分，还会进行其他滚动和选择。随着购买者的滚动，应用程序会一次显示一个产品，实际上它是使用可滚动的游标在结果集内上下浏览。

可以通过多种方式使用游标：

  - 不用于任何行。

  - 用于一个表中的部分行或所有行。

  - 用于逻辑联接表中的所有行或部分行。

  - 在游标或字段级别是只读或可更新的。

  - 仅向前或完全可滚动。

  - 用于服务器中的游标键集。

  - 对其他应用程序所导致的基础表更改（如成员关系、排序、插入、更新和删除）敏感。

  - 存在于服务器或客户端上。

只读游标可帮助用户浏览结果集，可读/写游标可用来实现单个行更新。复杂游标可以用指回到基表中行的键集来定义。某些游标在向前方向上是只读的，而另一些游标可以前后移动，并基于其他应用程序对数据库进行的更改来提供对结果集的动态刷新。

并非所有的应用程序都需要使用游标来访问或更新数据。一些查询完全不需要通过使用游标来直接更新行。在您检索数据时，应尽量选择除游标以外的其他技术；即使您使用游标技术，也应当选择影响最小的游标。当您使用存储过程创建结果集时，使用游标的编辑或更新方法不能更新结果集。

## <a name="concurrency"></a>并发

在某些多用户应用程序中，至关重要的是使显示给最终用户的数据尽可能最新。航空订票系统就是此类系统的一个典型示例，在该系统中，许多用户可能会争着预订给定航班上的同一个座位（也就是单个记录）。在这种情况下，应用程序在设计上必需能够处理针对单个记录的并发操作。

在其他应用程序中，并发不是那么重要。在这种情况下，使数据随时保持最新所涉及的资源耗费并无意义。

## <a name="position"></a>位置

游标还跟踪结果集内的当前位置。请将游标位置视为指向当前记录的指针，这与数组索引指向数组中特定位置的值的方式类似。

## <a name="scrollability"></a>可滚动性

应用程序所使用的游标类型还影响在结果集内的行之间能否向前和向后移动；有时，这也称为可滚动性。 将移动向前*和*向后在结果集中的功能将添加到游标的复杂性，因此增加实现成本。 因此，应当只在必要时才使用具有该功能的游标。

