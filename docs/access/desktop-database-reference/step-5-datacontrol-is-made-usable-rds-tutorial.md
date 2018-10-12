---
title: 步骤 5：使用 DataControl（RDS 教程）
TOCTitle: 'Step 5: DataControl is Made Usable (RDS Tutorial)'
ms:assetid: 9eff5732-2743-6891-dfa6-0991645e17ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249728(v=office.15)
ms:contentKeyID: 48546672
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1d9bd24d0aff1134a6af77862fd8f011d4ddff9f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25468293"
---
# <a name="step-5-datacontrol-is-made-usable-rds-tutorial"></a>步骤 5：使用 DataControl（RDS 教程）


**适用于**： Access 2013 |Office 2013

所返回的 **Recordset** 对象已经可以使用。可以像对任何其他 **Recordset** 一样检查、定位或编辑该对象。对 **Recordset** 可以执行的操作取决于相应的环境。Visual Basic 和 Visual C++ 具有一些可视控件，这些控件可以直接或通过启用数据控件间接使用 **Recordset** 。

例如，如果您正在使用 Microsoft Internet Explorer 显示网页，则可能希望在可视控件中显示 **Recordset** 对象数据。网页上的可视控件不能直接访问 **Recordset** 对象。但是，它们可以通过 **RDS.DataControl** 访问 [Recordset](datacontrol-object-rds.md) 对象。当 **RDS.DataControl** 的 [SourceRecordset](recordset-sourcerecordset-properties-rds.md) 属性设置为 **Recordset** 对象时，RDS.DataControl 便可被可视控件使用。

可视控件对象的 **DATASRC** 参数必须设置为 **RDS.DataControl** ，它的 **DATAFLD** 属性必须设置为 **Recordset** 对象字段（列）。

在本教程中，设置 **SourceRecordset** 属性：

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```
