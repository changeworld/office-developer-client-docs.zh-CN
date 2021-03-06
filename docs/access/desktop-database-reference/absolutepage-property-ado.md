---
title: AbsolutePage 属性 (ADO)
TOCTitle: AbsolutePage property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: a285f9f9533e4ecd903e6cc6c0e427bf44c84ca4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870532"
---
# <a name="absolutepage-property-ado"></a>AbsolutePage 属性 (ADO)

**适用于**： Access 2013、 Office 2013

指示当前记录驻留在哪一页。

## <a name="settings-and-return-values"></a>设置和返回值

设置或返回一个**Long**值从 1 到[Recordset](recordset-object-ado.md)对象 ([PageCount](pagecount-property-ado.md)) 中的页面数或返回[PositionEnum](positionenum.md)值之一。

## <a name="remarks"></a>备注

此属性可用于标识当前记录所在的页的页码。它使用 [PageSize](pagesize-property-ado.md) 属性将 **Recordset** 对象的总行集计数逻辑划分为一系列页，每一页中都包含与 **PageSize** 相等的记录数（最后一页除外，该页的记录数可以小于这个数）。提供程序必须支持相应的功能，此属性才可用。

获取或设置 **AbsolutePage** 属性时，ADO 将根据以下情况将 [AbsolutePosition](absoluteposition-property-ado.md) 属性与 [PageSize](pagesize-property-ado.md) 属性结合使用：

- 若要获取 **AbsolutePage** ，ADO 将首先检索 **AbsolutePosition** ，然后用它除以 **PageSize** 。

- 若要设置 **AbsolutePage** ，ADO 将按照以下方式移动 **AbsolutePosition** ：它将 **PageSize** 乘以新 **AbsolutePage** 值，然后向该值加 1。 因此之后成功设置**AbsolutePage** , **Recordset**中的当前位置是该页面中的第一个记录。

和 **AbsolutePosition** 属性一样， **AbsolutePage** 将从 1 开始，当前记录为 **Recordset** 中的第一条记录时，它等于 1。设置此属性，可以移动到特定页的第一条记录处。可从 **PageCount** 属性获得总页数。

