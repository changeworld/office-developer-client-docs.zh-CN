---
title: SetField 宏操作
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 66dfe95aaa335e14b0148d2fcd610abc30556e3a
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997495"
---
# <a name="setfield-macro-action"></a>SetField 宏操作

**适用于**： Access 2013、 Office 2013

**SetField** 操作可用于向字段分配值。

> [!NOTE]
> [!注释] **SetField** 操作仅适用于数据宏。

## <a name="setting"></a>设置

下表列出了 **SetField** 操作的相关参数。

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
<td><p><strong>Name</strong></p></td>
<td><p>一个用于标识字段的字符串。</p></td>
</tr>
<tr class="even">
<td><p><strong>值</strong></p></td>
<td><p>一个表达式，指定要分配到的域的值。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注释

无法在 [**CreateRecord**](createrecord-data-block.md) 或 [**EditRecord**](editrecord-data-block.md) 数据块外部使用 **SetField** 操作。

