---
title: Relation.Table 属性 (DAO)
TOCTitle: Table Property
ms:assetid: cc4f64ef-c4e9-1a14-9263-5f8220d89840
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834423(v=office.15)
ms:contentKeyID: 48547736
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053068
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dd6f1ef3ea1d955f3b17d4cafb7e521c54191d27
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929578"
---
# <a name="relationtable-property-dao"></a>Relation.Table 属性 (DAO)


**适用于**： Access 2013、 Office 2013

指示 **[Relation](relation-object-dao.md)** 对象的主表的名称。该属性应当等同于 **[TableDef](connection-name-property-dao.md)** 或 **[QueryDef](tabledef-object-dao.md)** 对象的 **[Name](querydef-object-dao.md)** 属性设置（仅适用于 Microsoft Access 工作区）。

## <a name="syntax"></a>语法

*表达式*。表

*表达式*一个代表**Relation**对象的变量。

## <a name="remarks"></a>注解

对于新的尚未追加到集合中的 **Relation** 对象， **Table** 属性设置是可读写的；对于 [**Relations**](relations-collection-dao.md) 集合中的现有 **Relation** 对象，该属性设置是只读的。

将 **Table** 属性与 **[ForeignTable](relation-foreigntable-property-dao.md)** 属性一起使用，可以定义 **Relation** 对象（该对象表示两个表或查询中的字段间的关系）。将 **Table** 属性设置为主 **TableDef** 或 **QueryDef** 对象的 **Name** 属性设置，将 **ForeignTable** 属性设置为外部（引用） **TableDef** 或 **QueryDef** 对象的 **Name** 属性设置。 **[Attributes](field-attributes-property-dao.md)** 属性决定了两个对象之间的关系类型。

例如，如果您有一个存储在 ValidParts 表中的有效部件代码列表（这些代码存储在名为 PartNo 的字段中），则可以与 OrderItem 表建立一对多关系，这样一来，如果部件代码输入到 OrderItem 表中，它就会出现在 ValidParts 表中。如果部件代码不存在于 ValidParts 表中，并且您未将 **Relation** 对象的 **Attributes** 属性设置为 **dbRelationDontEnforce**，就会发生可捕获的错误。

在本例中，ValidParts 表是主表，所以 **Relation** 对象的 **Table** 属性将设置为 ValidParts， **Relation** 对象的 **ForeignTable** 属性将设置为 OrderItem。 **Relation** 对象的 [**Fields**](field-object-dao.md) 集合中的 ****Field**** 对象的 [Name](fields-collection-dao.md) 和 **ForeignName** 属性将设置为 PartNo。

## <a name="example"></a>示例

以下示例演示 **Table**、 **ForeignTable** 和 **ForeignName** 属性如何定义两个表之间的 **Relation** 条件。

```vb
    Sub ForeignNameX() 
     
     Dim dbsNorthwind As Database 
     Dim relLoop As Relation 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Debug.Print "Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print ".Table - .Fields(0).Name" 
     Debug.Print " Foreign (Many) "; 
     Debug.Print ".ForeignTable - .Fields(0).ForeignName" 
     
     ' Enumerate the Relations collection of the Northwind 
     ' database to report on the property values of 
     ' the Relation objects and their Field objects. 
     For Each relLoop In dbsNorthwind.Relations 
     With relLoop 
     Debug.Print 
     Debug.Print .Name & " Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print .Table & " - " & .Fields(0).Name 
     Debug.Print " Foreign (Many) "; 
     Debug.Print .ForeignTable & " - " & _ 
     .Fields(0).ForeignName 
     End With 
     Next relLoop 
     
     dbsNorthwind.Close 
     
    End Sub
```
