---
title: AddNew 方法示例 (VB)
TOCTitle: AddNew method example (VB)
ms:assetid: 4ba53857-b5ad-d377-98c6-57992f9d69ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249238(v=office.15)
ms:contentKeyID: 48544697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7c19e12077c42d9487d6410793f07a6fa2c4bb18
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885610"
---
# <a name="addnew-method-example-vb"></a>AddNew 方法示例 (VB)


**适用于**： Access 2013、 Office 2013

以下示例使用 [AddNew](addnew-method-ado.md) 方法创建一个具有指定名称的新记录。

```vb 
 
'BeginAddNewVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim Cnxn As ADODB.Connection 
 Dim rstEmployees As ADODB.Recordset 
 Dim strCnxn As String 
 Dim strSQL As String 
 'record variables 
 Dim strID As String 
 Dim strFirstName As String 
 Dim strLastName As String 
 Dim blnRecordAdded As Boolean 
 
 ' Open a connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open Employees Table with a cursor that allows updates 
 Set rstEmployees = New ADODB.Recordset 
 strSQL = "Employees" 
 rstEmployees.Open strSQL, strCnxn, adOpenKeyset, adLockOptimistic, adCmdTable 
 
 ' Get data from the user 
 strFirstName = Trim(InputBox("Enter first name:")) 
 strLastName = Trim(InputBox("Enter last name:")) 
 
 ' Proceed only if the user actually entered something 
 ' for both the first and last names 
 If strFirstName <> "" And strLastName <> "" Then 
 
 rstEmployees.AddNew 
 rstEmployees!firstname = strFirstName 
 rstEmployees!LastName = strLastName 
 rstEmployees.Update 
 blnRecordAdded = True 
 
 ' Show the newly added data 
 MsgBox "New record: " & rstEmployees!EmployeeId & " " & _ 
 rstEmployees!firstname & " " & rstEmployees!LastName 
 
 Else 
 MsgBox "Please enter a first name and last name." 
 End If 
 
 ' Delete the new record because this is a demonstration 
 Cnxn.Execute "DELETE FROM Employees WHERE EmployeeID = '" & strID & "'" 
 
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
'EndAddNewVB 
```

