---
title: Field2.ValidationText Property (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d971b14093dd02204327e6f0ef30a81c6567c5bc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25468758"
---
# <a name="field2validationtext-property-dao"></a>Field2.ValidationText Property (DAO)


**适用于**： Access 2013 |Office 2013

设置或返回一个值，该值指定当 **Field2** 对象的值不符合 **ValidationRule** 属性设置指定的验证规则时，应用程序显示的消息文本（仅适用于 Microsoft Access 工作区）。可读写 **String**。

## <a name="syntax"></a>语法

*表达式*。ValidationText

*表达式*一个代表**Field2**对象的变量。

## <a name="remarks"></a>注解

设置或返回值是一个 **String**，用于指定当用户试图为字段输入无效值时显示的文本。对于尚未追加到集合中的对象，该属性是可读写的。

对于 **Field2** 对象， **ValidationText** 属性的用法取决于包含 [Field2](fields-collection-dao.md) 对象所追加到的 ****Fields**** 集合的对象。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>对象追加到</p></th>
<th><p>用法</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong></p></td>
<td><p>不支持</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
<td><p>只读</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>只读</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong></p></td>
<td><p>不支持</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>读/写</p></td>
</tr>
</tbody>
</table>
