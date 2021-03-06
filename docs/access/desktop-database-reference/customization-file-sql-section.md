---
title: 自定义文件 SQL 节
TOCTitle: Customization File SQL section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d314b37ee24f22e6abd76cdd855e7b3d5adaff0b
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945402"
---
# <a name="customization-file-sql-section"></a>自定义文件 SQL 节


**适用于**： Access 2013、 Office 2013

**sql** 节可以包含新的 SQL 字符串，该字符串用于替换客户端命令字符串。如果节中没有 SQL 字符串，将忽略该节。

新的 SQL 字符串可能是*参数化的*。就是说，**sql** 节 SQL 字符串（由“?”字符指定）中的参数可以替换为客户端命令字符串（由括号中的以逗号分隔的列表指定）中的 *identifier* 中的相应参数。标识符和参数列表的行为类似函数调用。

例如，假定客户端命令字符串为"CustomerByID(4)"，SQL 节标头为\[SQL CustomerByID\] ，和新的 SQL 节字符串是"选择\*FROM Customers WHERE CustomerID = ?"。 处理程序将生成、 SQL 节标头是\[SQL CustomerByID\] ，和新的 SQL 节字符串是"选择\*FROM Customers WHERE CustomerID = ?"。 处理程序将生成"选择\*FROM Customers WHERE CustomerID = 4"并使用该字符串来查询数据源。

如果新的 SQL 语句是空字符串 ("")，将忽略该节。

如果新的 SQL 语句字符串无效，则语句的执行将失败。实际上会忽略客户端参数。您可以有意这样做，以便"关闭"所有客户端 SQL 命令，如下所示：

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a>语法

替换 SQL 字符串项的格式为：

**SQL = * sqlString***

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
<td><p><strong>SQL</strong></p></td>
<td><p>字面字符串，用于指示这是 SQL 节项。</p></td>
</tr>
<tr class="even">
<td><p><strong><em>sqlString</em></strong></p></td>
<td><p>SQL 字符串，用于替换客户端字符串。</p></td>
</tr>
</tbody>
</table>

