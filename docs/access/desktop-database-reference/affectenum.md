---
title: AffectEnum （访问桌面数据库参考 （英文）
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ffb2ab2abbd24a19ddc433b5fd315dd535fd2a0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25466758"
---
# <a name="affectenum"></a>AffectEnum


**适用于**： Access 2013 |Office 2013

指定操作会影响哪些记录。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>常量</p></th>
<th><p>值</p></th>
<th><p>说明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adAffectAll</strong></p></td>
<td><p>3</p></td>
<td><p>如果未对 <strong>Recordset</strong> 应用任何 <a href="filter-property-ado.md">Filter</a>，则所有记录都受影响。
 如果将<strong>Filter</strong>属性设置为字符串条件 (如&quot;作者 = 'Smith'&quot;)，则该操作将影响当前章节中的可见记录。 如果将 <strong>Filter</strong> 属性设置为 <a href="filtergroupenum.md">FilterGroupEnum</a> 的成员或书签数组，则该操作将影响 <strong>Recordset</strong> 的所有行。</p>

> [!NOTE]
> <P>adAffectAll 在 Visual Basic 对象浏览器中处于隐藏状态。</P>


</td>
</tr>
<tr class="even">
<td><p><strong>adAffectAllChapters</strong></p></td>
<td><p>4</p></td>
<td><p>影响 <strong>Recordset</strong> 的所有同级章节中的全部记录，包括通过当前所应用的任何 <strong>Filter</strong> 都看不到的记录。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adaffectcurrent:</strong></p></td>
<td><p>1</p></td>
<td><p>只影响当前的记录。</p></td>
</tr>
<tr class="even">
<td><p><strong>adAffectGroup</strong></p></td>
<td><p>2</p></td>
<td><p>只影响满足当前 <a href="filter-property-ado.md">Filter</a> 属性设置的记录。必须将 <strong>Filter</strong> 属性设置为 <strong>FilterGroupEnum</strong> 值或 <strong>Bookmarks</strong> 数组，才能使用此选项。</p></td>
</tr>
</tbody>
</table>


**ADO/WFC 等效值**

包： **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>常量</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.Affect.ALL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Affect.ALLCHAPTERS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Affect.CURRENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Affect.GROUP</p></td>
</tr>
</tbody>
</table>
