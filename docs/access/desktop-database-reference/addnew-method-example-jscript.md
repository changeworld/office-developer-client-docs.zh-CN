---
title: AddNew 方法示例 (JScript)
TOCTitle: AddNew method example (JScript)
ms:assetid: b6f7e98d-d34d-dc2a-bdcb-65452f3fe5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249882(v=office.15)
ms:contentKeyID: 48547290
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7d7e3455612952c386898a00bbc1a7629113acc9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869342"
---
# <a name="addnew-method-example-jscript"></a>AddNew 方法示例 (JScript)

**适用于**： Access 2013、 Office 2013

以下示例使用 [AddNew](addnew-method-ado.md) 方法创建一个具指定名称的新记录。将以下代码剪切并粘贴到记事本或其他文本编辑器中，并另存为 **AddNewJS.asp** 。

```javascript
<!-- BeginAddNewJS --> 
<%@LANGUAGE="JScript" %> 
<!-- Include file for JScript ADO Constants --> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<html> 
 
<head> 
 <title>Add New method example (JScript)</title> 
<style> 
<!-- 
body { 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 BACKGROUND-COLOR:white; 
 COLOR:black; 
 } 
--> 
</style> 
</head> 
 
<body> 
<h1>AddNew method example (JScript)</h1> 
 
<% 
 if (Request.Form("Addit") == "AddNew") 
 { 
 // connection and recordset variables 
 var Cnxn = Server.CreateObject("ADODB.Connection") 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='Northwind';Integrated Security='SSPI';"; 
 var rsEmployee = Server.CreateObject("ADODB.Recordset"); 
 //record variables 
 var FName = String(Request.Form("FirstName")); 
 var LName = String(Request.Form("LastName")); 
 
 try 
 { 
 // open connection 
 Cnxn.Open(strCnxn) 
 
 // open Employee recordset using client-side cursor 
 rsEmployee.CursorLocation = adUseClient; 
 rsEmployee.Open("Employees", strCnxn, adOpenKeyset, adLockOptimistic, adCmdTable); 
 
 rsEmployee.AddNew(); 
 rsEmployee("FirstName") = FName; 
 rsEmployee("LastName") = LName; 
 rsEmployee.Update; 
 
 // of course, you would normally do error handling here 
 Response.Write("New record added.") 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // clean up 
 if (rsEmployee.State == adStateOpen) 
 rsEmployee.Close; 
 if (Cnxn.State == adStateOpen) 
 Cnxn.Close; 
 rsEmployee = null; 
 Cnxn = null; 
 } 
 } 
%> 
 
<form method="post" action="AddNewJS.asp" id=form1 name=form1> 
<table> 
<tr> 
 <td colspan="2"> 
 <h4>Please enter the record to add:</h4> 
 </td> 
</tr> 
<tr> 
 <td> 
 First Name: 
 </td> 
 <td> 
 <input name="FirstName" maxLength=20> 
 </td> 
</tr> 
<tr> 
 <td> 
 Last Name: 
 </td> 
 <td> 
 <input name="LastName" size="30" maxLength=30> 
 </td> 
</tr> 
<tr> 
 <td align="right"> 
 <input type="submit" value="Submit" name="Submit"> 
 </td> 
 <TD align="left"> 
 <INPUT type="reset" value="Reset" name="Reset"> 
 </TD> 
</tr> 
</table> 

<INPUT type="hidden" value="AddNew" name="Addit"> 
</form> 
</body> 
</HTML> 
<!-- EndAddNewJS --> 
 
```

