---
title: 唯一表，Unique Schema Unique Catalog 动态属性 (ADO)
TOCTitle: Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)
ms:assetid: e6374782-755b-322b-21de-6d6a386dcd98
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250169(v=office.15)
ms:contentKeyID: 48548374
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b2c3c87a820638b74e74c513443261e052e2c4d7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919428"
---
# <a name="unique-table-unique-schema-unique-catalog-dynamic-properties-ado"></a>唯一表，Unique Schema Unique Catalog 动态属性 (ADO)


**适用于**： Access 2013、 Office 2013

支持对 [Recordset](recordset-object-ado.md)（通过多个基表上的 JOIN 操作形成）中特定基表的修改进行严密控制。

  - **Unique Table** 指定允许在其上进行更新、插入和删除的基表的名称。

  - **Unique Schema** 指定该表的所有者的*架构*或名称。

  - **Unique Catalog** 指定包含该表的数据库的*目录*或名称。

## <a name="settings-and-return-values"></a>设置和返回值

设置或返回一个表示表、架构或目录的名称的 **String** 值。

## <a name="remarks"></a>备注

所需的基表由其目录、架构和表名称唯一标识。当设置了 **Unique Table** 属性时， **Unique Schema** 或 **Unique Catalog** 属性的值将用于查找基表。可以（但并不要求）在设置 **Unique Table** 属性前先设置 **Unique Schema** 和/或 **Unique Catalog** 属性。

**Unique Table** 的主键将作为整个 **Recordset** 的主键处理。任何需要使用主键的方法都将使用此键。

设置 **Unique Table** 时， [Delete](delete-method-ado-recordset.md) 方法仅影响指定的表。 [AddNew](addnew-method-ado.md)、[Resync](resync-method-ado.md)、[Update](update-method-ado.md) 和 [UpdateBatch](updatebatch-method-ado.md) 方法会影响 **Recordset** 所有相关的基础基表。

在进行任何自定义的重新同步操作前，必须指定 **Unique Table** 。如果尚未指定 **Unique Table** ， [Resync Command](resync-command-property-dynamic-ado.md) 属性将不起任何作用。

如果不能找到唯一的基表，则将导致出现运行时错误。

这些动态属性都将在 **CursorLocation** 属性设置为 [adUseClient](properties-collection-ado.md) 时追加到 [Recordset](cursorlocation-property-ado.md) 对象的 **Properties** 集合中。

