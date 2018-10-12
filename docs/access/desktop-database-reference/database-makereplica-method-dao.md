---
title: Database.MakeReplica Method (DAO)
TOCTitle: MakeReplica Method
ms:assetid: b6bf4982-0804-12ce-849f-d2b4ac2e48a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822413(v=office.15)
ms:contentKeyID: 48547286
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053371
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8596548389b066b6ff11e7103090ef50906d79a9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25468350"
---
# <a name="databasemakereplica-method-dao"></a>Database.MakeReplica Method (DAO)

**适用于**： Access 2013 |Office 2013

根据另一个数据库副本制作一个新的副本（仅适用于 Microsoft Access 工作区）。

## <a name="syntax"></a>语法

*表达式*。MakeReplica （***路径名***，在***说明***中，***选项***）

*表达式*一个代表**Database**对象的变量。

### <a name="parameters"></a>参数

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
<td><p>PathName</p></td>
<td><p>必需</p></td>
<td><p><strong>字符串</strong></p></td>
<td><p>新副本的路径和文件名。如果 replica 是一个现有的文件名，则会发生错误。</p></td>
</tr>
<tr class="even">
<td><p>说明</p></td>
<td><p>必需</p></td>
<td><p><strong>字符串</strong></p></td>
<td><p>一个 <strong>String</strong>，用于描述所创建的副本</p></td>
</tr>
<tr class="odd">
<td><p>选项</p></td>
<td><p>可选</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>一个<strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong>常量，指定要创建的副本的特征。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注解

新建部分副本的所有 **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** 属性都将设置为 **False**，表示不会将任何数据放入表中。

## <a name="example"></a>示例

此函数使用 **MakeReplica** 方法创建现有设计母版的附加副本。 IntOptions 参数可以是组合的常量**dbRepMakeReadOnly**和**dbRepMakePartial**，也可以是 0。 例如，若要创建只读的部分副本，您应传递值**dbRepMakeReadOnly** + **dbRepMakePartial**作为 intOptions 的值。

```vb 
Function MakeAdditionalReplica(strReplicableDB As _ 
 String, strNewReplica As String, intOptions As _ 
 Integer) As Integer 
 
 Dim dbsTemp As Database 
 On Error GoTo ErrorHandler 
 
 Set dbsTemp = OpenDatabase(strReplicableDB) 
 
 ' If no options are passed to 
 ' MakeAdditionalReplica, omit the 
 ' options argument, which defaults to 
 ' a full, read/write replica. Otherwise, 
 ' use the value of intOptions. 
 
 If intOptions = 0 Then 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB 
 Else 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB, _ 
 intOptions 
 End If 
 
 dbsTemp.Close 
 
ErrorHandler: 
 Select Case Err 
 Case 0: 
 MakeAdditionalReplica = 0 
 Exit Function 
 Case Else: 
 MsgBox "Error " & Err & " : " & Error 
 MakeAdditionalReplica = Err 
 Exit Function 
 End Select 
 
End Function 
 
```
