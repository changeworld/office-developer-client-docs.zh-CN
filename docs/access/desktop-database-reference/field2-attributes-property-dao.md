---
title: Field2.Attributes 属性 (DAO)
TOCTitle: Attributes Property
ms:assetid: 08ae9b6b-21e4-9b7e-0852-cfc6639027a7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845025(v=office.15)
ms:contentKeyID: 48543102
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052896
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2456fb3741cfe5871b46e7937619b060fd350b09
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922396"
---
# <a name="field2attributes-property-dao"></a>Field2.Attributes 属性 (DAO)


**适用于**： Access 2013、 Office 2013


设置或返回一个值，该值指示 **Field2** 对象的一个或多个特征。 **Long** 类型，可读写。

## <a name="syntax"></a>语法

*表达式*。属性

*表达式*一个代表**Field2**对象的变量。

## <a name="remarks"></a>注解

此值指定 **Field2** 对象所代表的字段的特征，并且可以是这些常量的组合。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>常量</p></th>
<th><p>说明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbAutoIncrField</strong></p></td>
<td><p>新记录的字段值将自动增加到无法更改的唯一 Long 类型整数（在 Microsoft Access 工作区中，只受 Microsoft Access 数据库引擎数据库表的支持）。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDescending</strong></p></td>
<td><p>字段将以降序（Z 到 A，或 100 到 0）排序；此选项只适用于 <strong>Index</strong> 对象的 <strong>Fields</strong> 集合中的 <strong>Field2</strong> 对象。如果省略此常量，将以升序（A 到 Z，或 0 到 100）排序。这是 <strong>Index</strong> 和 <strong>TableDef</strong> 字段的默认值（仅适用于 Microsoft Access 工作区）。.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFixedField</strong></p></td>
<td><p>该字段大小是固定的（“数字”字段的默认值）。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbHyperlinkField</strong></p></td>
<td><p>该字段包含超链接信息（仅适用于“备注”字段）。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSystemField</strong></p></td>
<td><p>该字段存储副本的复制信息；不能删除该字段类型（仅适用于 Microsoft Access 工作区）。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbUpdatableField</strong></p></td>
<td><p>可以更改该字段值。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVariableField</strong></p></td>
<td><p>该字段大小可变（仅适用于“文本”字段）。</p></td>
</tr>
</tbody>
</table>


对于尚未追加到集合中的对象，该属性是可读写的。对于已追加的 **Field2** 对象， **Attributes** 属性的可用性取决于包含 **Fields** 集合的对象。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>如果 Field 对象属于</p></th>
<th><p>则 Attributes</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong> 对象</p></td>
<td><p>将 <strong>Index</strong> 所要追加到的 <strong>TableDef</strong> 对象追加到 <strong>Database</strong> 对象之前是可读写的；追加后，该属性是只读的。</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong>对象</p></td>
<td><p>只读</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong>对象</p></td>
<td><p>只读</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong>对象</p></td>
<td><p>不支持</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong>对象</p></td>
<td><p>可读写</p></td>
</tr>
</tbody>
</table>


设置多个属性时，可通过对相应的常量求和来组合这些属性。将忽略所有无效值，且不产生错误。

## <a name="example"></a>示例

以下示例显示 Northwind 数据库中的 **Field2**、 **Relation** 和 **TableDef** 对象的 **Attributes** 属性。

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field2 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

