---
title: DeleteRecord 宏操作
TOCTitle: DeleteRecord macro action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 052e7a489eaec526db1552ced89b095f65f652df
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921584"
---
# <a name="deleterecord-macro-action"></a>DeleteRecord 宏操作

**适用于**： Access 2013、 Office 2013

可以使用 **DeleteRecord** 操作删除记录。

## <a name="setting"></a>设置

**DeleteRecord** 数据块具有以下参数。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>参数</p></th>
<th><p>说明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Record Alias</strong></p></td>
<td><p>一个用于标识要删除的记录的字符串。如果未指定 <em>Alias</em> 参数，则会删除当前记录。</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>注释

您可以使用 **LastCreateRecordIdentity** 本地变量来处理在 **CreateRecord** 数据块中创建的最后一条记录。 例如，使用以下语法引用最近创建的记录：

`[LastCreateRecordIdentity]`

