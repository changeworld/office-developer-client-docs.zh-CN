---
title: ConnectPromptEnum （访问桌面数据库参考 （英文）
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 387e9a853a306b2375034359ce26db50685afcc4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887906"
---
# <a name="connectpromptenum"></a>ConnectPromptEnum

**适用于**： Access 2013、 Office 2013

用于指定在打开到数据源的连接时是否应显示对话框，以提示缺少的参数。

<br/>

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
<td><p><strong>adPromptAlways</strong></p></td>
<td><p>1</p></td>
<td><p>始终提示。</p></td>
</tr>
<tr class="even">
<td><p><strong>adPromptComplete</strong></p></td>
<td><p>2</p></td>
<td><p>当需要更多信息时提示。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPromptCompleteRequired</strong></p></td>
<td><p>3</p></td>
<td><p>当需要更多信息但不允许可选参数时提示。</p></td>
</tr>
<tr class="even">
<td><p><strong>adPromptNever</strong></p></td>
<td><p>4</p></td>
<td><p>从不提示。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC 等效值

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
<td><p>AdoEnums.ConnectPrompt.ALWAYS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectPrompt.COMPLETE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ConnectPrompt.COMPLETEREQUIRED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectPrompt.NEVER</p></td>
</tr>
</tbody>
</table>

