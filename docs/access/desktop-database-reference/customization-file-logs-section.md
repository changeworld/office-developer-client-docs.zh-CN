---
title: 自定义文件 Logs 节
TOCTitle: Customization File Logs section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c9a8b9c2255825b135fbc181900a73b3686c64c7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946145"
---
# <a name="customization-file-logs-section"></a>自定义文件 Logs 节

**适用于**： Access 2013、 Office 2013

**logs** 节包含日志文件项，该项指定用于在 **DataFactory** 的操作期间记录错误的文件的名称。

## <a name="syntax"></a>语法

日志文件项的格式为：

`err=FileName`

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>部分</p></th>
<th><p>说明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>err</strong></p></td>
<td><p>字面字符串，用于指示这是日志文件项。</p></td>
</tr>
<tr class="even">
<td><p><em>FileName</em></p></td>
<td><p>完整路径和文件名。典型的文件名是 <strong>c:\msdfmap.log</strong>。</p></td>
</tr>
</tbody>
</table>


日志文件将包含每个错误的用户名、HRESULT、日期和时间。

