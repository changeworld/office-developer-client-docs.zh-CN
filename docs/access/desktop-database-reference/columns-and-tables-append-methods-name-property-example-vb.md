---
title: Columns 和 Tables 的 Append 方法、Name 属性示例 (VB)
TOCTitle: Columns and Tables Append Methods, Name Property Example (VB)
ms:assetid: 39458400-f30c-0636-19f2-c2c2788a6534
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249140(v=office.15)
ms:contentKeyID: 48544238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ffd2fe2843e28ab1411d51d3b7dd4c0a2938b3b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25467567"
---
# <a name="columns-and-tables-append-methods-name-property-example-vb"></a>Columns 和 Tables 的 Append 方法、Name 属性示例 (VB)


**适用于**： Access 2013 |Office 2013

下面的代码演示如何创建新表。

```vb 
 
' BeginCreateTableVB 
Sub Main() 
 On Error GoTo CreateTableError 
 
 Dim tbl As New Table 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Catalog. 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 tbl.Name = "MyTable" 
 tbl.Columns.Append "Column1", adInteger 
 tbl.Columns.Append "Column2", adInteger 
 tbl.Columns.Append "Column3", adVarWChar, 50 
 cat.Tables.Append tbl 
 Debug.Print "Table 'MyTable' is added." 
 
 'Delete the table as this is a demonstration. 
 cat.Tables.Delete tbl.Name 
 Debug.Print "Table 'MyTable' is deleted." 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set tbl = Nothing 
 Exit Sub 
 
CreateTableError: 
 
 Set cat = Nothing 
 Set tbl = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndCreateTableVB 
```
