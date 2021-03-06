---
title: AddNew 方法示例 (VBScript)
TOCTitle: AddNew method example (VBScript)
ms:assetid: a01f01ca-44a7-8743-394d-ef2c4b0919ca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249735(v=office.15)
ms:contentKeyID: 48546699
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f33b9f594404a96553825b04f86e94f2aa6c150
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870070"
---
# <a name="addnew-method-example-vbscript"></a>AddNew 方法示例 (VBScript)


**适用于**： Access 2013、 Office 2013

以下示例使用 [AddNew](addnew-method-ado.md) 方法创建一个具指定名称的新记录。

在 Active Server Page (ASP) 中使用下面的示例。 使用 **Find** 来查找文件 Adovbs.inc 并将其放置在要使用的目录中。 剪切和粘贴到记事本或其他文本编辑器，以下代码并将其保存为**AddNewVBS.asp**。 您可以在任何客户端浏览器中查看结果。

若要实际使用此示例，请 HTML 窗体中添加一条新记录。 单击“新增”****。 请参阅[Delete 方法示例](delete-method-example-vbscript.md)以移除不需要的记录。

```vb
 
<!-- BeginAddNewVBS --> 
<%@Language = VBScript %> 
<%' use this meta tag instead of adovbs.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
<HTML> 
<HEAD> 
    <TITLE>ADO AddNew Method (VBScript)</TITLE> 
    <STYLE> 
    <!-- 
    body { 
       font-family: 'Verdana','Arial','Helvetica',sans-serif; 
       BACKGROUND-COLOR:white; 
       COLOR:black; 
        } 
    TH { 
       background-color: #008080;  
       font-family: 'Arial Narrow','Arial',sans-serif;  
       font-size: xx-small; 
       color: white; 
       } 
    TD {  
       text-align: center; 
       background-color: #f7efde; 
       font-family: 'Arial Narrow','Arial',sans-serif;  
       font-size: xx-small; 
        } 
    --> 
    </STYLE> 
</HEAD> 
<BODY>  
 
<H1>ADO AddNew Method (VBScript)</H1> 
 
<% ' to integrate/test this code replace the  
   ' Data Source value in the Connection string%> 
<%  
    ' connection and recordset variables 
    Dim Cnxn, strCnxn 
    Dim rsCustomers, strSQLCustomers 
    Dim fld, Err 
 
    ' open connection 
    Set Cnxn = Server.CreateObject("ADODB.Connection") 
    strCnxn = "Provider='sqloledb';Data Source=" & _ 
            Request.ServerVariables("SERVER_NAME") & ";" & _ 
            "Integrated Security='SSPI';Initial Catalog='Northwind';" 
    Cnxn.Open strCnxn 
         
     ' create and open Recordset using object refs 
    Set rsCustomers = Server.CreateObject("ADODB.Recordset") 
    strSQLCustomers = "Customers" 
     
    rsCustomers.ActiveConnection = Cnxn 
    rsCustomers.CursorLocation = adUseClient 
    rsCustomers.CursorType = adOpenKeyset 
    rsCustomers.LockType = adLockOptimistic 
    rsCustomers.Source = strSQLCustomers 
    rsCustomers.Open 
 
    'If this is first time page is open, Form collection 
    'will be empty when data is entered. run AddNew method 
    If Not IsEmpty(Request.Form) Then 
        If Not Request.Form("CompanyName") = "" Then 
            rsCustomers.AddNew 
                rsCustomers("CustomerID") = Request.Form("CompanyID") 
                rsCustomers("CompanyName") = Request.Form("CompanyName") 
                rsCustomers("ContactName") = Request.Form("FirstName") & _ 
                    " " & Request.Form("LastName") 
                rsCustomers("Phone") = Request.Form("PhoneNumber") 
                rsCustomers("City") = Request.Form("City") 
                rsCustomers("Region") = Request.Form("State") 
            rsCustomers.Update 
             ' check for errors 
            If Cnxn.Errors.Count > 0 Then 
                For Each Err In Cnxn.Errors 
                    Response.Write("Error " & Err.SQLState & ": " & _ 
                        Err.Description & " | " & Err.NativeError) 
                Next 
            Cnxn.Errors.Clear 
            rsCustomers.CancelUpdate 
            End If 
            'On Error GoTo 0 
        rsCustomers.MoveFirst 
        End If 
    End If 
%> 
 
<TABLE COLSPAN="8" CELLPADDING=5 BORDER=1 ALIGN="center"> 
<!-- BEGIN column header row for Customer Table--> 
    <TR> 
        <TH>Customer ID</TH> 
        <TH>Company Name</TH> 
        <TH>Contact Name</TH> 
        <TH>Phone Number</TH> 
        <TH>City</TH> 
        <TH>State/Province</TH> 
        </TR> 
         
    <% ' show the data 
        Do Until rsCustomers.EOF 
            Response.Write("<TR>") 
            Response.Write("<TD>" & rsCustomers("CustomerID") & "</TD>") 
            Response.Write("<TD>" & rsCustomers("CompanyName")& "</TD>") 
            Response.Write("<TD>" & rsCustomers("ContactName") & "</TD>") 
            Response.Write("<TD>" & rsCustomers("Phone") & "</TD>") 
            Response.Write("<TD>" & rsCustomers("City") & "</TD>") 
            Response.Write("<TD>" & rsCustomers("Region") & "</TD>") 
            Response.Write("</TR>") 
        rsCustomers.MoveNext  
        Loop  
    %> 
</TABLE>  
 
<HR> 
 
<!-- 
    Form to enter new record posts variables 
    back to this page 
--> 
<FORM Method=post Action="AddNewVbs.asp" Name=Form> 
    <TABLE> 
        <TR> 
            <TD>Company ID:</TD> 
            <TD><INPUT Size="5" Name="CompanyID" maxLength=5  ></TD> 
        </TR> 
        <TR> 
            <TD>Company Name:</TD> 
            <TD><INPUT Size="50" Name="CompanyName" ></TD> 
        </TR> 
        <TR> 
            <TD>Contact First Name:</TD> 
            <TD><INPUT Size="50" Name="FirstName" ></TD> 
        </TR> 
        <TR> 
            <TD>Contact Last Name:</TD> 
            <TD><INPUT Size="50" Name="LastName" ></TD> 
        </TR> 
        <TR> 
            <TD>Contact Phone:</TD> 
            <TD><INPUT Size="50" Name="PhoneNumber" ></TD> 
        </TR> 
        <TR> 
            <TD>City:</TD> 
            <TD><INPUT Size="50" Name="City" ></TD> 
        </TR> 
        <TR> 
            <TD>State / Province:</TD> 
            <TD><INPUT Size="5" Name="State" ></TD> 
        </TR> 
        <TR> 
            <TD Align="right"><INPUT Type="submit" Value="Add New"></TD> 
            <TD Align="left"><INPUT Type="reset" Value="Reset Form"></TD> 
        </TR> 
    </TABLE> 

</FORM> 
 
<% 
    ' show connection 
    Response.Write("Following is the connection string: <br><br>") 
    Response.Write(Cnxn) 
 
    ' Clean up. 
    If rsCustomers.State = adStateOpen then 
       rsCustomers.Close 
    End If 
    If Cnxn.State = adStateOpen then 
       Cnxn.Close 
    End If 
    Set rsCustomers=Nothing 
    Set Cnxn=Nothing 
    Set fld=Nothing 
%> 
 
<SCRIPT Language = "VBScript"> 
Sub Form_OnSubmit 
   MsgBox "Sending New Record to Server",,"ADO-ASP _Example" 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
<!-- EndAddNewVBS --> 
```

