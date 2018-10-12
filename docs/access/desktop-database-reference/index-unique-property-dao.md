---
title: Index.Unique Property (DAO)
TOCTitle: Unique Property
ms:assetid: a4486da5-8a1a-b4fc-0e07-e65cd2e726f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821087(v=office.15)
ms:contentKeyID: 48546809
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052990
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bf2bbd8e1bf5c7c51d93e0669becbfd093e29994
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25468225"
---
# <a name="indexunique-property-dao"></a>Index.Unique Property (DAO)

**适用于**： Access 2013 |Office 2013

设置或返回一个值，该值指示 **[Index](index-object-dao.md)** 对象是否代表一个表的唯一（键）索引（仅适用于 Microsoft Access 工作区）。

## <a name="syntax"></a>语法

*表达式*。唯一

*表达式*一个代表**Index**对象的变量。

## <a name="remarks"></a>注解

该属性设置是可读写的，只有在对象追加到集合中后，它才变为只读。

唯一索引包含一个或多个字段，这些字段可以按预定义的唯一顺序对表中的所有记录进行逻辑排列。如果索引由一个字段组成，则该字段中的值在整个表中必须是唯一的。如果索引包含多个字段，则每个字段中可以出现重复值，但是由所有索引字段中的值组成的每个组合必须是唯一的。

如果 **Index** 对象的 [Unique](index-primary-property-dao.md) 和 ****Primary**** 属性都设置为 **True**，则索引是唯一的，并且是主要索引：它按预定义的逻辑顺序唯一标识表中的所有记录。如果 **Primary** 属性设置为 **False**，则索引是次要索引。次要索引（键和非键）按预定义顺序对记录进行逻辑排列，但不作为表中记录的标识符。


> [!NOTE]
> <UL>
> <LI>
> <P>您不必为表创建索引，但是在大型的未添加索引的表中，访问特定记录可能会花费很长时间。</P>
> <LI>
> <P>从不含索引的表中检索的记录没有特定返回顺序。</P>
> <LI>
> <P><A href="field-attributes-property-dao.md">Index</A> 对象中每个 <A href="field-object-dao.md"><STRONG>Field</STRONG></A> 对象的 <STRONG><STRONG>Attributes</STRONG></STRONG> 属性决定了记录的顺序，因此决定了对该 <STRONG>Index</STRONG> 对象使用的访问技术。</P>
> <LI>
> <P>唯一索引有助于优化记录的查找。</P>
> <LI>
> <P>索引不影响基表的实际顺序，只影响当选择特定索引时或 Microsoft Access 数据库引擎创建 <A href="recordset-object-dao.md">Recordset</A> 对象时表类型 <STRONG><STRONG>Recordset</STRONG></STRONG> 对象访问记录的方式。</P></LI></UL>



## <a name="example"></a>示例

以下示例将新 **Index** 对象的 **Unique** 属性设置为 **True**，并将 Index 追加到 Employees 表的 **Indexes** 集合中。然后，以下示例枚举 **TableDef** 的 **Indexes** 集合和每个 **Index** 的 **Properties** 集合。新 **Index** 只允许一个记录带有 **TableDef** 中的 Country、LastName 和 FirstName 的特定组合。

```vb
    Sub UniqueX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim idxNew As Index 
       Dim idxLoop As Index 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set tdfEmployees = dbsNorthwind!Employees 
     
       With tdfEmployees 
          ' Create and append new Index object to the Indexes  
          ' collection of the Employees table. 
          Set idxNew = .CreateIndex("NewIndex") 
     
          With idxNew 
             .Fields.Append .CreateField("Country") 
             .Fields.Append .CreateField("LastName") 
             .Fields.Append .CreateField("FirstName") 
             .Unique = True 
          End With 
     
          .Indexes.Append idxNew 
          .Indexes.Refresh 
     
          Debug.Print .Indexes.Count & " Indexes in " & _ 
             .Name & " TableDef" 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In .Indexes 
             Debug.Print "  " & idxLoop.Name 
     
             ' Enumerate Properties collection of each Index  
             ' object. 
             For Each prpLoop In idxLoop.Properties 
                Debug.Print "    " & prpLoop.Name & _ 
                   " = " & IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          Next idxLoop 
     
          ' Delete new Index because this is a demonstration. 
          .Indexes.Delete idxNew.Name 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```