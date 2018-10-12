---
title: Property Object (DAO)
TOCTitle: Property Object
ms:assetid: a1ecb0db-bb93-a7b5-23c3-0b73f275dfe0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820932(v=office.15)
ms:contentKeyID: 48546744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0ee7efa4b25fe25bac728ce0c8d0dcd5ea8747b4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25466897"
---
# <a name="property-object-dao"></a>Property Object (DAO)


**适用于**： Access 2013 |Office 2013

**Property** 对象代表 DAO 对象的内部特征或用户定义特征。

## <a name="remarks"></a>注解

除 **Connection** 和 **Error** 对象外，每个 DAO 对象都包含一个 **Properties** 集合，该集合具有与该 DAO 对象的内置属性相对应的 **Property** 对象。用户也可以定义 **Property** 对象，并将其追加到某些 DAO 对象的 **Properties** 集合。这些 **Property** 对象（通常就称为属性）唯一地描述了对象的该实例。

可以为下列对象创建用户定义属性：

  - **Database**、 **Index**、 **QueryDef** 和 **TableDef** 对象

  - **QueryDef** 和 **TableDef** 对象的 **Fields** 集合中的 **Field** 对象

要添加用户定义属性，请使用 **CreateProperty** 方法创建一个具有唯一的 **Name** 属性设置的 **Property** 对象。创建新的 **Property** 对象的 **Type** 和 **Value** 属性，然后将该对象追加到相应对象的 **Properties** 集合。要为其添加用户定义属性的对象必须已经追加到集合中。如果引用尚未追加到 **Properties** 集合的用户定义的 **Property** 对象，则会发生错误；如果将用户定义的 **Property** 对象追加到包含同名 **Property** 对象的 **Properties** 集合中，也会发生错误。

可以从 **Properties** 集合中删除用户定义属性，但是不能删除内置属性。


> [!NOTE]
> <P>[!注释] 一个用户定义的 <STRONG>Property</STRONG> 对象只与一个对象的特定实例相关联。属性并不是为选定类型的对象的所有实例定义的。</P>



可以使用对象的 **Properties** 集合来枚举该对象的内置属性和用户定义属性。不需要事先确切地知道存在哪些属性或其特征（**Name** 和 **Type** 属性）是什么，就可处理这些属性。但是，如果尝试读取一个只写属性（例如 **Workspace** 对象的 **Password** 属性），或尝试读取或写入不适当的上下文中的属性（例如 **TableDef** 对象的 **Fields** 集合中的 **Field** 对象的 **Value** 属性设置），则会发生错误。

**Property** 对象还包括四个内置属性：

  - **Name** 属性，一个 **String**，用于对属性进行唯一标识。

  - **Type** 属性，一个 **Integer**，用于指定属性数据类型。

  - **Value** 属性，一个 **Variant**，包含了属性设置。

  - **Inherited** 属性，一个 **Boolean**，指示属性是否是从另一个对象继承的。例如， **Recordset** 对象的 **Fields** 集合中的 **Field** 对象可以从 **TableDef** 或 **QueryDef** 基础对象继承属性。

若要按照序号或 **Name** 属性设置来引用集合中的内置 **Property** 对象，可以使用下列任何一种语法形式：

  - * 对象 ***。属性**(0)

  - *对象 ***。属性**("* 名称 *")

  - *对象 ***。属性**\!* 名称 *\]

对于内置属性，还可以使用以下语法：

  - *对象*。*名称*


> [!NOTE]
> <P>对于用户定义的属性，您必须使用完整的<EM>对象</EM><STRONG>。属性</STRONG>（"<EM>name</EM>"） 语法。</P>



使用同样的语法格式，还可以引用 **Property** 对象的 **Value** 属性。引用的上下文将确定是引用 **Property** 对象自身，还是引用 **Property** 对象的 **Value** 属性。
