---
title: Recordset.MoveNext Method (DAO)
TOCTitle: MoveNext Method
ms:assetid: 0a1315cf-92f8-b8ef-1542-081e8c2d5be0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845090(v=office.15)
ms:contentKeyID: 48543142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7675da7016044836bd2c8bf723ab6e1bc9a65b1b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25466551"
---
# <a name="recordsetmovenext-method-dao"></a>Recordset.MoveNext Method (DAO)


**适用于**： Access 2013 |Office 2013

移到指定的 **Recordset** 对象中的下一条记录，并使该记录成为当前记录。

## <a name="syntax"></a>语法

*表达式*。MoveNext

*表达式*一个表示**Recordset**对象的变量。

## <a name="remarks"></a>注解

使用 **Move** 方法可以在记录间移动，而不需要应用条件。

如果要编辑当前记录，请确保使用 **Update** 方法保存更改，然后移到另一条记录。如果在不更新的情况下移到另一条记录，则更改将会丢失，且不发出警告。

在打开 **Recordset** 时，第一条记录将是当前记录，并且 **BOF** 属性为 **False**。如果 **Recordset** 不包含记录，则 **BOF** 属性为 **True**，并且不存在当前记录。

如果最后一条记录是当前记录，在使用 **MoveNext** 时， **EOF** 属性将是 **True**，并且不会有当前记录。如果再次使用 **MoveNext**，将发生错误，同时 **EOF** 保留为 **True**。

如果 recordset 引用表类型**Recordset** （仅限 Microsoft Access 工作区），则移动遵循当前索引。 可以使用 **Index** 属性设置当前索引。 如果不设置当前索引，则返回记录的顺序将是不确定的。

不能对仅向前类型**Recordset**对象使用**MoveFirst**、 **MoveLast**和**MovePrevious**方法。

若要将 **Recordset** 对象中的当前记录的位置向前或向后移动指定的记录数，请使用 **Move** 方法。
