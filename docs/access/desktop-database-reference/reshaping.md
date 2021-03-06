---
title: 调整形状 （访问桌面数据库参考 （英文）
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 49a61e72a4d9260b73275d84ce912ebc76f37652
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996452"
---
# <a name="reshaping"></a>重构

**适用于**： Access 2013、 Office 2013

可以向 Shape 命令的子句所创建的 **Recordset** 赋予一个*别名*（通常用 AS 关键字）。已构形的 **Recordset** 的别名可以在一个完全不同的命令中引用。即，您可以再次使用以前构形的 **Recordset**，也可以用新的 Shape 命令对其*重新构形*。为了支持此功能，ADO 提供了一个属性：[Reshape Name](reshape-name-property-dynamic-ado.md)。

重新构形具有两个主要功能，第一个功能是将现有的 **Recordset** 与新的父 **Recordset** 相关联。

## <a name="example"></a>示例

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

第二个功能是允许进行非章节访问现有的子**Recordset**对象，使用语法`"SHAPE <recordset reshape name>"`。

> [!NOTE]
> [!注释] 不能向现有的 **Recordset** 追加列，不能用任何干扰性 COMPUTE 子句对参数化 **Recordset** 或 **Recordset** 对象进行重新构形，不能从正重新构形的 **Recordset** 对任何 **Recordset** 后代执行聚合运算。 改变了形状的**Recordset**和新的形状命令都必须使用相同 * *[Connection](connection-object-ado.md)对象。


