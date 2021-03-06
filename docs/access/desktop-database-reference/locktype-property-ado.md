---
title: LockType 属性 (ADO)
TOCTitle: LockType property (ADO)
ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15)
ms:contentKeyID: 48543589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88657361d6ce5ac168f21f5709bdaf68eeb23b6d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879053"
---
# <a name="locktype-property-ado"></a>LockType 属性 (ADO)


**适用于**： Access 2013、 Office 2013

指示编辑过程中为记录设置的锁定类型。

## <a name="settings-and-return-values"></a>设置和返回值

设置或返回一个 [LockTypeEnum](locktypeenum.md) 值。默认值为 **adLockReadOnly** 。

## <a name="remarks"></a>备注

在打开 **Recordset** 前设置 [LockType](recordset-object-ado.md) 属性可指定在打开该记录集时提供程序应使用的锁定类型。读取该属性将返回在打开的 **Recordset** 对象上使用的锁定类型。

提供程序可能不支持所有锁定类型。如果某个提供程序不能支持请求的 **LockType** 设置，则将用其他锁定类型替代。若要确定 **Recordset** 对象可用的实际锁定功能，请在 [adUpdate](supports-method-ado.md) 和 **adUpdateBatch** 中使用 **Supports** 方法。

如果 **CursorLocation** 属性设置为 [adUseClient](cursorlocation-property-ado.md) ，则不支持 **adLockPessimistic** 设置。如果设置不受支持的值，则不会产生错误，因为此时将改用最接近的受支持的 **LockType** 。

**Recordset** 关闭时 **LockType** 属性为可读/写属性，而打开时为只读属性。

**远程数据服务用法**当客户端 Recordset 对象上使用时， **LockType**属性可以仅可设为**adLockBatchOptimistic**。

