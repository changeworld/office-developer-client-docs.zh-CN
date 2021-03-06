---
title: CursorLocation 属性 (ADO)
TOCTitle: CursorLocation property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 874662585292b9d9a9b2bc53f5b6fe5178e3517b
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025845"
---
# <a name="cursorlocation-property-ado"></a>CursorLocation 属性 (ADO)


**适用于**： Access 2013、 Office 2013

指示游标服务的位置。

## <a name="settings-and-return-values"></a>设置和返回值

设置或返回一个 **Long** 值，该值可以设置为 [CursorLocationEnum](cursorlocationenum.md) 值之一。

## <a name="remarks"></a>备注

此属性允许在提供程序可访问的各种游标库间进行选择。通常，可以选择使用客户端游标库或位于服务器上的游标库。

此属性设置仅影响在设置了该属性后建立的连接。更改 **CursorLocation** 属性对现有的连接没有影响。

[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) 方法返回的游标将继承此设置。 **Recordset** 对象将从其关联的连接自动继承此设置。

此属性在 [Connection](connection-object-ado.md) 或已关闭的 [Recordset](recordset-object-ado.md) 上为可读/写属性，而在打开的 **Recordset** 上为只读属性。

**远程数据服务用法**客户端**Recordset**或**Connection**对象上时，**会在 CursorLocation**属性可以仅将设置为**adUseClient**。

