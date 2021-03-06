---
title: 确定受支持的功能
TOCTitle: Determining what is supported
ms:assetid: 47b44dc9-e0fd-f204-0c68-e0de9247ee2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249221(v=office.15)
ms:contentKeyID: 48544602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3b2db5fbdf0d85ee48b9dbc494ccce6022bfb165
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946585"
---
# <a name="determining-what-is-supported"></a>确定受支持的功能

**适用于**： Access 2013、 Office 2013

**Supports** 方法用于确定指定的 **Recordset** 对象是否支持特定类型的功能。它的语法如下：

`boolean = recordset.Supports( CursorOptions )`

**Supports** 返回布尔值，以指示提供程序是否支持 *CursorOptions* 参数所标识的所有功能。可以使用 **Supports** 方法来确定 **Recordset** 对象支持哪些类型的功能。如果 **Recordset** 对象支持其相应常量在 *CursorOptions* 中的功能，则 **Supports** 方法返回 **True**。否则，它返回 **False**。

通过使用 **Supports** 方法，可以检查 **Recordset** 对象是否有添加新记录、使用书签、使用 **Find** 方法、使用滚动、使用 **Index** 属性和执行批更新等功能。有关常量及其含义的完整列表，请参阅 [CursorOptionEnum](cursoroptionenum.md)。

尽管对于给定功能 **Supports** 方法可能返回 **True** ，但并不能保证提供程序在所有环境下都能提供此功能。 **Supports** 方法只是返回在满足某些条件的情况下提供程序是否支持指定的功能。例如， **Supports** 方法可以指示 **Recordset** 对象支持更新，即使游标基于多表联接 - 其中的某些列是不可更新的。

