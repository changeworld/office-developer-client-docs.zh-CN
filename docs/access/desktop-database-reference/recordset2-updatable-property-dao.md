---
title: Recordset2.Updatable 属性 (DAO)
TOCTitle: Updatable Property
ms:assetid: ad8184b6-ffe3-dde6-ddee-4b23cdaa9c59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821726(v=office.15)
ms:contentKeyID: 48547041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 871d92937bb7793b09d1520d2bf3fa33b61fcaf4
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919337"
---
# <a name="recordset2updatable-property-dao"></a>Recordset2.Updatable 属性 (DAO)


**适用于**： Access 2013、 Office 2013

返回一个值，该值指示是否可以更改 DAO 对象。只读 **Boolean**。

## <a name="syntax"></a>语法

*表达式*。可更新

*表达式*一个表示**Recordset2**对象的变量。

## <a name="remarks"></a>说明

快照和转发-仅类型 Recordset 对象始终返回**False**。

许多类型的对象都可以包含不能更新的字段。例如，您可以创建动态集类型的 **Recordset** 对象，在该对象中只能更改某些字段。这些字段可能是固定的，也可能包含自动递增的数据，或者动态集可以从合并可更新表和不可更新表的查询中得出。

如果该对象仅包含只读字段，则 **Updatable** 属性的值为 **False**。当一个或多个字段可更新时，属性的值为 **True**。您只能编辑可更新的字段。如果尝试向只读字段分配新值，则会发生可捕获的错误。

由于可更新的对象可以包含只读字段，因此请在编辑记录之前检查 **Recordset** 对象的 **Fields** 集合中每个字段的 **DataUpdatable** 属性。

