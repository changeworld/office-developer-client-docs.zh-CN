---
title: OpenDiagram 宏操作
TOCTitle: OpenDiagram macro action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b04870a416874e2136e21b40c62d8e64a6182efe
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998544"
---
# <a name="opendiagram-macro-action"></a>OpenDiagram 宏操作

**适用于**： Access 2013、 Office 2013

在 Access 项目中，可以使用 **OpenDiagram** 操作在设计视图中打开数据库图表。

> [!NOTE]
> [!注释] 如果数据库不受信任，将不允许此操作。 

## <a name="setting"></a>设置

**OpenDiagram** 操作具有以下参数。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>操作参数</p></th>
<th><p>说明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>图表名称</strong></p></td>
<td><p>要打开的数据库图表的名称。 宏生成器窗格的<strong>图表名称</strong>框在<strong>操作参数</strong>部分中显示当前数据库中的所有数据库图表。 这是必需参数。 如果在类库数据库中运行包含 <strong>OpenDiagram</strong> 操作的宏，Microsoft Access 将先在该类库数据库中查找具有此名称的图表，然后再在当前数据库中查找。</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>说明

此操作类似于在导航窗格中双击数据库图表，或在导航窗格中右键单击数据库图表并单击 **"设计视图"**。

> [!TIP]
> [!提示] 您可以将数据库图表从导航窗格拖至某个宏操作行。这会自动创建在设计视图中打开该数据库图表的 **OpenDiagram** 操作。

要在 Visual Basic for Applications (VBA) 模块中运行 **OpenDiagram** 操作，请使用 **DoCmd** 对象的 **OpenDiagram** 方法。

