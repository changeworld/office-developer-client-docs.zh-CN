---
title: Append 方法 (ADOX Keys)
TOCTitle: Append Method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d7e10e272155d2d0377810bf8aa1704a30bad39
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2018
ms.locfileid: "25468417"
---
# <a name="append-method-adox-keys"></a>Append 方法 (ADOX Keys)


**适用于**： Access 2013 |Office 2013


将新的 [Key](key-object-adox.md) 对象添加到 [Keys](keys-collection-adox.md) 集合。

## <a name="syntax"></a>语法

*键*。追加*密钥* \[，*关键字类型*\] \[，*列*\] \[，*RelatedTable* \] \[，*RelatedColumn*\]

## <a name="parameters"></a>参数

  - *Key*

  - 要追加的 **Key** 对象，或者要创建并追加的键的名称。

  - *关键字类型*

  - 可选。 指定键类型的 **Long** 值。 *Key*参数对应于**Key**对象的[Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\))属性。

  - *Column*

  - 可选。 **String** 值，指定要进行索引的列的名称。 *Columns*参数对应于一个[Column](column-object-adox.md)对象的[Name](name-property-adox.md)属性的值。

  - *RelatedTable*

  - 可选。 指定相关表的名称的 **String** 值。 *RelatedTable*参数对应于一个[Table](table-object-adox.md)对象的**Name**属性的值。

  - *RelatedColumn*

  - 可选。 **String** 值，指定外键的相关列的名称。RelatedColumn 参数对应于 **Column** 对象的 **Name** 属性值。

## <a name="remarks"></a>备注

*Columns*参数可接受的列的名称或列名的数组。
