---
title: UnderlyingValue 属性 (ADO)
TOCTitle: UnderlyingValue property (ADO)
ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15)
ms:contentKeyID: 48548782
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d91dccb88ff39ad344ffa0e59e7ccdaaa9f1565
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867781"
---
# <a name="underlyingvalue-property-ado"></a>UnderlyingValue 属性 (ADO)


**适用于**： Access 2013、 Office 2013



指示数据库中 [Field](field-object-ado.md) 对象的当前值。

## <a name="return-value"></a>返回值

返回一个指示 **Field** 的值的 **Variant** 值。

## <a name="remarks"></a>备注

使用 **UnderlyingValue** 属性可以返回数据库中的当前字段的值。 **UnderlyingValue** 属性中的字段值是事务可见的值，而且可能是其他事务所进行的最近更新的结果。此值可能不同于 [OriginalValue](originalvalue-property-ado.md) 属性，后者反映的是最初返回到 [Recordset](recordset-object-ado.md) 的值。

这类似于使用 [Resync](resync-method-ado.md) 方法，但是 **UnderlyingValue** 属性仅返回当前记录中的特定字段的值。该值与 [Resync](resync-method-ado.md) 方法用于替换 [Value](value-property-ado.md) 属性的值相同。

将此属性与 **OriginalValue** 属性结合使用时，可以解决因批更新而引发的冲突。

## <a name="record"></a>Record

对于调用 [Update](record-object-ado.md) 之前添加的字段，此属性将为空（适用于 [Record](update-method-ado.md) 对象）。

