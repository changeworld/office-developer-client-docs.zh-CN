---
title: NumericScale 和 Precision 属性示例 (VB)
TOCTitle: NumericScale and Precision properties example (VB)
ms:assetid: 728a76a3-1f80-935b-b6c7-94255ffe0160
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249462(v=office.15)
ms:contentKeyID: 48545610
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc1dd570a1b2fbb3b178216e6b1742aaeb682947
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882075"
---
# <a name="numericscale-and-precision-properties-example-vb"></a>NumericScale 和 Precision 属性示例 (VB)


**适用于**： Access 2013、 Office 2013

本示例演示 [Column](numericscale-property-adox.md) 对象的 [NumericScale](precision-property-adox.md) 和 [Precision](column-object-adox.md) 属性。 此代码将显示*Northwind*数据库的**订单明细**表及其值。

```vb 
 
' BeginNumericScalePrecVB 
Sub Main() 
 On Error GoTo NumericScalePrecXError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim tblOD As ADOX.Table 
 Dim colLoop As ADOX.Column 
 
 ' Connect the catalog. 
 cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "data source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 Set cat.ActiveConnection = cnn 
 
 ' Retrieve the Order Details table 
 Set tblOD = cat.Tables("Order Details") 
 
 ' Display numeric scale and precision of 
 ' small integer fields. 
 For Each colLoop In tblOD.Columns 
 If colLoop.Type = adSmallInt Then 
 MsgBox "Column: " & colLoop.Name & vbCr & _ 
 "Numeric scale: " & _ 
 colLoop.NumericScale & vbCr & _ 
 "Precision: " & colLoop.Precision 
 End If 
 Next colLoop 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
NumericScalePrecXError: 
 Set cat = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndNumericScalePrecVB 
```

