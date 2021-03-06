---
title: Children 属性 (ADO MD)
TOCTitle: Children property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b93081c577a0d93d442706f231dace5e7865976
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927702"
---
# <a name="children-property-ado-md"></a>Children 属性 (ADO MD)


**适用于**： Access 2013、 Office 2013

返回层次结构中将当前 [Member](members-collection-ado-md.md) 作为父级的 [Members](member-object-ado-md.md) 集合。

## <a name="return-values"></a>返回值

返回一个 **Members** 集合，并且该值为只读。

## <a name="remarks"></a>说明

**Children** 属性包含将当前 **Member** 作为层次结构父级的 **Members** 集合。叶级 **Member** 对象在该 **Members** 集合中没有子成员。此属性仅在属于 **Level** 对象的 [Member](level-object-ado-md.md) 对象上受支持。通过属于 **Position** 对象的 [Member](position-object-ado-md.md) 对象引用此属性时，会发生错误。

