---
title: FilterAxis 属性 (ADO MD)
TOCTitle: FilterAxis Property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 912dfec595f718c2144e69b4fbd3af592f8b6d5b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25466741"
---
# <a name="filteraxis-property-ado-md"></a>FilterAxis 属性 (ADO MD)


**适用于**： Access 2013 |Office 2013

指示有关当前单元格集的筛选信息。

## <a name="return-values"></a>返回值

返回一个 [Axis](axis-object-ado-md.md) 对象，并且该值为只读。

## <a name="remarks"></a>说明

使用 **FilterAxis** 属性可返回与将数据切片时所用的维度有关的信息。 [Axis](dimensioncount-property-ado-md.md) 的 **DimensionCount** 属性返回切片器的维数。此轴通常只有一行。

**FilterAxis** 返回的 [Axis](filteraxis-property-ado-md.md) 不包含在 [Cellset](axes-collection-ado-md.md) 对象的 [Axes](cellset-object-ado-md.md) 集合中。
