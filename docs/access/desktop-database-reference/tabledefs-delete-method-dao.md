---
title: TableDefs.Delete 方法 (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d511155f7a5fe1e6b83092e2065302bab99765b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999006"
---
# <a name="tabledefsdelete-method-dao"></a>TableDefs.Delete 方法 (DAO)

**适用于**： Access 2013、 Office 2013

从 **TableDefs** 集合中删除指定的 **TableDef** 对象。

## <a name="syntax"></a>语法

*表达式*。删除 （***名称***）

*表达式*一个代表**TableDefs**对象的变量。

## <a name="parameters"></a>参数

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>必需/可选</p></th>
<th><p>数据类型</p></th>
<th><p>说明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>必需</p></td>
<td><p><strong>字符串</strong></p></td>
<td><p>要删除的 TableDef 的名称。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注解

仅当**TableDef**对象的新且未被追加到数据库，或者**TableDef**的**可更新**属性设置为**True**时，才支持 Delete 方法。

