---
title: QueryDef.Prepare Property (DAO)
TOCTitle: Prepare Property
ms:assetid: d5a285c4-bd00-028b-b785-f1890db29bab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835035(v=office.15)
ms:contentKeyID: 48547968
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101187
f1_categories:
- Office.Version=v15
ms.openlocfilehash: cec1fde6bc76438da2292ae30545337eaeea6cf4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25466987"
---
# <a name="querydefprepare-property-dao"></a>QueryDef.Prepare Property (DAO)


**适用于**： Access 2013 |Office 2013

## <a name="syntax"></a>语法

*表达式*。准备

*表达式*一个代表**QueryDef**对象的变量。

## <a name="remarks"></a>注解

可以使用 **Prepare** 属性让服务器从您的查询创建并执行临时存储过程，也可以直接执行查询。默认情况下， **Prepare** 属性设置为 **dbQPrepare**。但是，您可以将该属性设置为 **dbQUnprepare**，以禁止准备查询。在此情况下，将使用 **SQLExecDirect** API 执行查询。

创建存储过程可能降低初始操作的速度，但是提高了对该查询的所有后续引用的性能。不过，某些查询不能以存储过程的形式来执行。在这种情况下，您必须将 **Prepare** 属性设置为 **dbQUnprepare**。

如果**Prepare**设置为**dbQPrepare**，这可以通过将**[Execute](querydef-execute-method-dao.md)** 方法的 options 参数设置为**一设置**执行查询时覆盖。


> [!NOTE]
> <P>[!注释] 一旦设置了 DAO <A href="querydef-sql-property-dao.md"><STRONG>SQL</STRONG></A> 属性，就会调用 ODBC <STRONG>SQLPrepare</STRONG> API。因此，如果您希望使用 <STRONG>dbQUnprepare</STRONG> 选项来提高性能，则必须在设置 <STRONG>SQL</STRONG> 属性之前设置 <STRONG>Prepare</STRONG> 属性。</P>



## <a name="example"></a>示例

以下示例使用 **Prepare** 属性指定应当直接执行查询，而不是首先在服务器上创建临时存储过程。

```vb 
Sub PrepareX() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' object. 
 Set wrkODBC = CreateWorkspace("", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Set qdfTemp = conPubs.CreateQueryDef("") 
 
 With qdfTemp 
 ' Because you will only run this query once, specify 
 ' the ODBC SQLExecDirect API function. If you do 
 ' not set this property before you set the SQL 
 ' property, the ODBC SQLPrepare API function will 
 ' be called anyway which will nullify any 
 ' performance gain. 
 .Prepare = dbQUnprepare 
 .SQL = "UPDATE roysched " & _ 
 "SET royalty = royalty * 2 " & _ 
 "WHERE title_id LIKE 'BU____' OR " & _ 
 "title_id LIKE 'PC____'" 
 .Execute 
 End With 
 
 Debug.Print "Query results:" 
 
 ' Open recordset containing modified records. 
 Set rstTemp = conPubs.OpenRecordset( _ 
 "SELECT * FROM roysched " & _ 
 "WHERE title_id LIKE 'BU____' OR " & _ 
 "title_id LIKE 'PC____'") 
 
 ' Enumerate recordset. 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , !title_id, !lorange, _ 
 !hirange, !royalty 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 conPubs.Close 
 wrkODBC.Close 
 
```
