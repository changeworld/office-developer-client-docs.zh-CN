---
title: ADO 对象和接口
TOCTitle: ADO objects and interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa301974b4b417d09b0439b3970ee366eeb5d06e
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910725"
---
# <a name="ado-objects-and-interfaces"></a>ADO 对象和接口

**适用于**： Access 2013、 Office 2013

ActiveX 数据对象 (ADO) 对象模型中都表示这些对象之间的关系。

每个对象可包含在其对应的集合中。 例如，[Error](error-object-ado.md) 对象可以包含在 [Errors](errors-collection-ado.md) 集合中。 有关详细信息，请参阅[ADO 集合](ado-collections.md)或特定集合主题。

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>对象</th>
<th>说明</th>
</tr>
<tr class="odd">
<td><p><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></p></td>
<td><p>在 C/C++ 应用程序中从 OLE DB <strong>Row</strong> 对象构建 ADO <strong>Record</strong> 对象。</p></td>
</tr>
<tr class="even">
<td><p><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></p></td>
<td><p>在 C/C++ 应用程序中从 OLE DB <strong>Rowset</strong> 对象构建 ADO <strong>Recordset</strong> 对象。</p></td>
</tr>
<tr class="odd">
<td><p><a href="error-object-ado.md">Command</a></p></td>
<td><p>定义要对数据源执行的特定命令。</p></td>
</tr>
<tr class="even">
<td><p><a href="field-object-ado.md">Connection</a></p></td>
<td><p>表示指向数据源的打开的连接。</p></td>
</tr>
<tr class="odd">
<td><p><a href="error-object-ado.md">Error</a></p></td>
<td><p>包含有关数据访问错误的详细信息，该错误与涉及提供程序的单个操作相关。</p></td>
</tr>
<tr class="even">
<td><p><a href="field-object-ado.md">Field</a></p></td>
<td><p>表示具有常规数据类型的数据列。</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameter-object-ado.md">参数</a></p></td>
<td><p>表示与基于参数化查询或存储过程的 <strong>Command</strong> 对象关联的参数或变量。</p></td>
</tr>
<tr class="even">
<td><p><a href="property-object-ado.md">属性</a></p></td>
<td><p>表示提供程序所定义的 ADO 对象的动态特征。</p></td>
</tr>
<tr class="odd">
<td><p><a href="record-object-ado.md">Record</a></p></td>
<td><p>表示 <strong>Recordset</strong> 的一行，或文件系统中的目录或文件。</p></td>
</tr>
<tr class="even">
<td><p><a href="recordset-object-ado.md">Recordset</a></p></td>
<td><p>表示从基表得到的整个记录集，或执行命令的结果。在任何时候， <strong>Recordset</strong> 对象只引用该集合中的单个记录作为当前记录。</p></td>
</tr>
<tr class="odd">
<td><p><a href="stream-object-ado.md">Stream</a></p></td>
<td><p>表示二进制数据流。</p></td>
</tr>
</tbody>
</table>

<br/>

