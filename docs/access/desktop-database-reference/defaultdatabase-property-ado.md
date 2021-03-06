---
title: DefaultDatabase 属性 (ADO)
TOCTitle: DefaultDatabase property (ADO)
ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15)
ms:contentKeyID: 48546784
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6238192f123e31c27a0e553d548be0b1623f0a32
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882327"
---
# <a name="defaultdatabase-property-ado"></a>DefaultDatabase 属性 (ADO)


**适用于**： Access 2013、 Office 2013

指示 [Connection](connection-object-ado.md) 对象的默认数据库。

## <a name="settings-and-return-values"></a>设置和返回值

设置或返回一个 **String** 值，该值可计算为提供程序中可用的数据库的名称。

## <a name="remarks"></a>备注

使用 **DefaultDatabase** 属性可以设置或返回特定 **Connection** 对象上的默认数据库的名称。

如果有默认数据库，SQL 字符串可以使用非限定性语法访问该数据库中的对象。若要访问 **DefaultDatabase** 属性中指定的数据库之外的其他数据库中的对象，必须使用所需的数据库名称来限定对象名称。进行连接时，提供程序会将默认数据库信息写入 **DefaultDatabase** 属性中。某些提供程序仅允许一个连接使用一个数据库，在这种情况下就不能更改 **DefaultDatabase** 属性。

某些数据源和提供程序可能不支持此功能，会返回错误或空字符串。

**远程数据服务用法**此属性不是在客户端**Connection**对象上可用。

