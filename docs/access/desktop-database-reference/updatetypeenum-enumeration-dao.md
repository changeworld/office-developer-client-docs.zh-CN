---
title: UpdateTypeEnum Enumeration (DAO)
TOCTitle: UpdateTypeEnum Enumeration
ms:assetid: 7ac38bae-27fc-f3d0-5b75-569bce547954
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196186(v=office.15)
ms:contentKeyID: 48545800
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ee8638d6fdade7e6955613964f619270574ce4b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25466760"
---
# <a name="updatetypeenum-enumeration-dao"></a>UpdateTypeEnum Enumeration (DAO)


**适用于**： Access 2013 |Office 2013

与 **Update** 方法一起用来指定要写入到磁盘中的更新。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>值</p></th>
<th><p>说明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbUpdateBatch</p></td>
<td><p>4</p></td>
<td><p>将更新缓存中的所有挂起的更改写入磁盘中。</p></td>
</tr>
<tr class="even">
<td><p>dbUpdateCurrentRecord</p></td>
<td><p>2</p></td>
<td><p>仅将当前记录的挂起更改写入磁盘中。</p></td>
</tr>
<tr class="odd">
<td><p>dbUpdateRegular</p></td>
<td><p>1</p></td>
<td><p>（默认值）挂起的更改不进行缓存，直接写入磁盘中。</p></td>
</tr>
</tbody>
</table>
