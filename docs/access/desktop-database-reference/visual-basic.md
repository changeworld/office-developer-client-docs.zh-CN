---
title: Visual Basic （访问桌面数据库参考 （英文）
TOCTitle: Visual Basic
ms:assetid: 9d153b6c-c860-7350-cb3c-b9bd08f75ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249714(v=office.15)
ms:contentKeyID: 48546616
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f496b39c3b06832cab9f60d2e560c9748f12c0d1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880556"
---
# <a name="visual-basic"></a>Visual Basic


**适用于**： Access 2013、 Office 2013

为了在 Microsoft Visual Basic 中处理 ADO 事件，必须使用 **WithEvents** 关键字声明模块级变量。该变量只能声明为类模块的一部分，并且必须在模块级别声明。但是，它所受限制并非看起来那样大，因为 Visual Basic **Form** 对象也是类。处理 ADO 事件的最简单方式是使用 **WithEvents** 声明变量。以下示例将处理 **Connection** 对象的 **ConnectComplete** 事件：

```vb 
 
' BeginEventExampleVB02 
Dim WithEvents connEvent As Connection 
Attribute connEvent.VB_VarHelpID = -1 
Dim strMsg As String 
 
Private Sub Form_Load() 
 On Error GoTo ErrHandler: 
 
 Dim strConn As String 
 
 ' Create a new object with event 
 ' handling enabled. 
 strConn = "Provider='sqloledb';" & _ 
 "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';" & _ 
 "Integrated Security='SSPI';" 
 Set connEvent = New ADODB.Connection 
 connEvent.Open strConn 
 
 Exit Sub 
 
ErrHandler: 
 MsgBox strMsg 
End Sub 
 
Private Sub connEvent_ConnectComplete(ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pConnection As ADODB.Connection) 
 
 If adStatus = adStatusErrorsOccurred Then 
 If Not pError Is Nothing Then 
 Select Case pError.Number 
 Case adErrOperationCancelled 
 ' The operation was cancelled in the 
 ' Will event. Notify the user and exit. 
 strMsg = "I'm sorry you can't connect right now." & vbCrLf 
 strMsg = strMsg & " Click OK to exit." 
 Unload Me 
 Case Else 
 strMsg = "Error " & Format(pError.Number) & vbCrLf 
 strMsg = strMsg & pError.Description 
 strMsg = strMsg & " Click OK to exit." 
 Unload Me 
 End Select 
 Else 
 strMsg = "Error occured. Click OK to exit." 
 Unload Me 
 End If 
 End If 
 'frmWait.btnOK.Enabled = True 
End Sub 
' EndEventExampleVB02 
```

**Connection** 对象声明于 **Form** 级别，并使用 **WithEvents** 关键字来启用事件处理。 窗体\_加载事件处理程序实际上会通过将新的**Connection**对象分配给*connEvent*创建对象，然后打开连接。 当然，实际的应用程序应在窗体中的多个处理\_加载事件处理程序不是如下所示。

