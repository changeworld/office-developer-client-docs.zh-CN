---
title: Recordset2.GetRows 方法 (DAO)
TOCTitle: GetRows Method
ms:assetid: e5c0a082-e9d2-359f-fed5-835ab91d2311
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835959(v=office.15)
ms:contentKeyID: 48548367
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 652bd4ce63164463d58f30a0259a7e4208f118ee
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998734"
---
# <a name="recordset2getrows-method-dao"></a>Recordset2.GetRows 方法 (DAO)

**适用于**： Access 2013、 Office 2013

检索 **[Recordset](recordset-object-dao.md)** 对象中的多行。

## <a name="syntax"></a>语法

*表达式*。GetRows (***NumRows***)

*表达式*一个表示**Recordset2**对象的变量。

## <a name="parameters"></a>参数

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名称</p></th>
<th><p>必需/可选</p></th>
<th><p>数据类型</p></th>
<th><p>说明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>NumRows</em></p></td>
<td><p>可选</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>要检索的行数。</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>返回值

Variant

## <a name="remarks"></a>注解

使用 **GetRows** 方法从 **Recordset** 复制记录。 **GetRows** 返回二维数组。 第一个下标标识字段，第二个下标标识行号。 例如，`intField`代表字段和`intRecord`标识行号：

`avarRecords(intField, intRecord)`

若要获取返回的第二行中的第一个字段值，请使用类似如下的代码：

`field1 = avarRecords(0,1)`

若要获取第一行中的第二个字段值，请使用类似如下的代码：

`field2 = avarRecords(1,0)`

**GetRows** 返回数据后，avarRecords 变量自动成为二维数组。

如果请求的行数多于可用行数，则 **GetRows** 仅返回可用行的数目。 由于数组的大小进行了调整以适合返回的行数，因此可以使用 Visual Basic for Applications **UBound** 函数确定 **GetRows** 实际上检索了多少行。 例如，如果将结果返回到**Variant**调用 varA 时，您可以使用下面的代码来确定实际返回多少行：

`numReturned = UBound(varA,2) + 1`

需要使用 "+ 1"，因为返回的第一行位于数组的 0 元素中。可以检索的行数受可用内存量的限制。如果表较大的话，不应使用 **GetRows** 将整个表检索到数组中。

由于 **GetRows** 将 **Recordset** 的所有字段返回到包括"备注"和"长二进制"型字段的数组中，因此可能需要使用能够限制返回字段的查询。

调用 **GetRows** 后，当前记录将被定位在下一个未读行上。 即**GetRows**具有**移动**numrows 对当前记录相同的效果。

如果尝试使用多个 **GetRows** 调用检索所有行，请使用 **[EOF](recordset2-eof-property-dao.md)** 属性，以确保位于 **Recordset** 的末尾。如果 **GetRows** 位于 **Recordset** 的末尾，或者无法在请求的范围内检索到某行，那么它返回的结果数将少于请求数目。例如，如果您尝试检索 10 条记录，但是无法检索第 5 条记录， **GetRows** 将返回 4 条记录，同时将第 5 条记录设置为当前记录。这不会生成运行时错误。如果另一个用户删除了动态集类型 **Recordset** 中的某条记录，则可能发生这种情况。有关如何处理这种情况的演示，请参阅示例。

## <a name="example"></a>示例

以下示例使用 **GetRows** 方法从 **Recordset** 中检索指定行数，并使用生成的数据填充数组。 **GetRows** 方法在以下两种情况下返回的行数少于所需的行数：已到达 **EOF**，或 **GetRows** 尝试检索已被其他用户删除的记录。只有当发生第二种情况时，函数才返回 **False**。若要使该过程运行，需要使用 GetRowsOK 函数。

```vb
    Sub GetRowsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strMessage As String 
     Dim intRows As Integer 
     Dim avarRecords As Variant 
     Dim intRecord As Integer 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT FirstName, LastName, Title " & _ 
     "FROM Employees ORDER BY LastName", dbOpenSnapshot) 
     
     With rstEmployees 
     Do While True 
     ' Get user input for number of rows. 
     strMessage = "Enter number of rows to retrieve." 
     intRows = Val(InputBox(strMessage)) 
     
     If intRows <= 0 Then Exit Do 
     
     ' If GetRowsOK is successful, print the results, 
     ' noting if the end of the file was reached. 
     If GetRowsOK(rstEmployees, intRows, _ 
     avarRecords) Then 
     If intRows > UBound(avarRecords, 2) + 1 Then 
     Debug.Print "(Not enough records in " & _ 
     "Recordset to retrieve " & intRows & _ 
     " rows.)" 
     End If 
     Debug.Print UBound(avarRecords, 2) + 1 & _ 
     " records found." 
     
     ' Print the retrieved data. 
     For intRecord = 0 To UBound(avarRecords, 2) 
     Debug.Print " " & _ 
     avarRecords(0, intRecord) & " " & _ 
     avarRecords(1, intRecord) & ", " & _ 
     avarRecords(2, intRecord) 
     Next intRecord 
     Else 
     ' Assuming the GetRows error was due to data 
     ' changes by another user, use Requery to 
     ' refresh the Recordset and start over. 
     If .Restartable Then 
     If MsgBox("GetRows failed--retry?", _ 
     vbYesNo) = vbYes Then 
     .Requery 
     Else 
     Debug.Print "GetRows failed!" 
     Exit Do 
     End If 
     Else 
     Debug.Print "GetRows failed! " & _ 
     "Recordset not Restartable!" 
     Exit Do 
     End If 
     End If 
     
     ' Because using GetRows leaves the current record 
     ' pointer at the last record accessed, move the 
     ' pointer back to the beginning of the Recordset 
     ' before looping back for another search. 
     .MoveFirst 
     Loop 
     End With 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function GetRowsOK(rstTemp As Recordset2, _ 
     intNumber As Integer, avarData As Variant) As Boolean 
     
     ' Store results of GetRows method in array. 
     avarData = rstTemp.GetRows(intNumber) 
     ' Return False only if fewer than the desired number of 
     ' rows were returned, but not because the end of the 
     ' Recordset was reached. 
     If intNumber > UBound(avarData, 2) + 1 And _ 
     Not rstTemp.EOF Then 
     GetRowsOK = False 
     Else 
     GetRowsOK = True 
     End If 
     
    End Function
```
