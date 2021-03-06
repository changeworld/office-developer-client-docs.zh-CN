---
title: AbsolutePage、PageCount 和 PageSize 属性示例 (VB)
TOCTitle: AbsolutePage, PageCount, and PageSize properties example (VB)
ms:assetid: bd13fb6c-8ee4-7475-ef2d-9067e30918de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249911(v=office.15)
ms:contentKeyID: 48547426
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 0b98557f4c5906c5d1952f635c9967e3b280cbae
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885071"
---
# <a name="absolutepage-pagecount-and-pagesize-properties-example-vb"></a>AbsolutePage、PageCount 和 PageSize 属性示例 (VB)


**适用于**： Access 2013、 Office 2013

此示例使用 [AbsolutePage](absolutepage-property-ado.md)、[PageCount](pagecount-property-ado.md) 和 [PageSize](pagesize-property-ado.md) 属性显示 ***Employees***（雇员）表中的姓名和雇用日期，每次显示五条记录。

```vb 
 
'BeginAbsolutePageVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim rstEmployees As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strSQL As String 
 'record variables 
 Dim strMessage As String 
 Dim intPage As Integer 
 Dim intPageCount As Integer 
 Dim intRecord As Integer 
 
 'Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open employee recordset 
 ' Use client cursor to enable AbsolutePosition property 
 Set rstEmployees = New ADODB.Recordset 
 strSQL = "employee" 
 rstEmployees.Open strSQL, strCnxn, adUseClient, adLockReadOnly, adCmdTable 
 
 ' Display names and hire dates, five records at a time 
 rstEmployees.PageSize = 5 
 intPageCount = rstEmployees.PageCount 
 For intPage = 1 To intPageCount 
 rstEmployees.AbsolutePage = intPage 
 strMessage = "" 
 For intRecord = 1 To rstEmployees.PageSize 
 strMessage = strMessage & _ 
 rstEmployees!fname & " " & _ 
 rstEmployees!lname & " " & _ 
 rstEmployees!hire_date & vbCr 
 rstEmployees.MoveNext 
 If rstEmployees.EOF Then Exit For 
 Next intRecord 
 MsgBox strMessage 
 Next intPage 
 
 ' clean up 
 rstEmployees.Close 
 Cnxn.Close 
 Set rstEmployees = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstEmployees Is Nothing Then 
 If rstEmployees.State = adStateOpen Then rstEmployees.Close 
 End If 
 Set rstEmployees = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndAbsolutePageVB 
```

