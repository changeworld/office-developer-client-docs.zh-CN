---
title: Field2.Value 属性 (DAO)
TOCTitle: Value Property
ms:assetid: 6ead6ba8-1613-99c7-7968-56f5b81b2385
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195566(v=office.15)
ms:contentKeyID: 48545515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e7c17992daff5064b41507f5c2a1b2781476095a
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936873"
---
# <a name="field2value-property-dao"></a>Field2.Value 属性 (DAO)


**适用于**： Access 2013、 Office 2013

设置或返回对象的值。可读/写 **Variant** 类型。

## <a name="syntax"></a>语法

*表达式*。值

*表达式*一个代表**Field2**对象的变量。

## <a name="remarks"></a>注解

设置或返回值是 Variant 数据类型，其计算结果值属于对象的 **Type** 属性所指定的数据类型。

通常， **Value** 属性用于检索和更改 **Recordset** 对象中的数据。

**Value** 属性是 **Field2**、 **Parameter** 和 **Property** 对象的默认属性。因此，您可以通过直接引用这些对象（而不是指定 **Value** 属性）来设置或返回这些对象之一的值。

如果尝试在不正确的上下文中设置或返回 **Value** 属性（例如 **TableDef** 对象的 **Fields** 集合中的 **Field2** 对象的 **Value** 属性），则会导致可捕获的错误。


> [!NOTE]
> 从 Microsoft SQL Server 数据库读取小数值时，在 Microsoft Access 工作区中将使用科学计数法设置这些值的格式，但是这些值在 ODBCDirect 工作区中仍显示为普通的小数值。


