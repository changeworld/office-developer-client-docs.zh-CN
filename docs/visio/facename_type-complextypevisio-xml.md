---
title: FaceName_Type 复杂类型 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 8035f541e619360403336bd2fbd931cf05dbfe59
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382440"
---
# <a name="facenametype-complextype-visio-xml"></a>FaceName_Type 复杂类型 (Visio XML)

## <a name="type-information"></a>类型信息

|||
|:-----|:-----|
|**命名空间** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**架构文件** <br/> |VisioSchema15 2012 06 05.xsd  <br/> |
|**扩展基** <br/> |无  <br/> |
   
## <a name="definition"></a>定义

```XML
      <xs:complexType name="FaceName_Type">
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="UnicodeRanges"
  type="xsd:string"
    />
    <xs:attribute name="CharSets"
  type="xsd:string"
    />
    <xs:attribute name="Panos"
  type="xsd:string"
    />
    <xs:attribute name="Panose"
  type="xsd:string"
    />
    <xs:attribute name="Flags"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>元素和属性

如果此架构定义了具体要求，如**sequence**， **minOccurs**、 **maxOccurs**和**choice**，请参阅定义部分。 
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="attributes"></a>属性

|**属性**|**类型**|**必需**|**说明**|**可能的值**|
|:-----|:-----|:-----|:-----|:-----|
|CharSets  <br/> |xsd: string  <br/> |可选  <br/> ||Xsd: string 类型的值。  <br/> |
|Flags  <br/> |xsd:unsignedInt  <br/> |可选  <br/> ||Xsd:unsignedInt 类型的值。  <br/> |
|NameU  <br/> |xsd: string  <br/> |必需  <br/> ||Xsd: string 类型的值。  <br/> |
|Panos  <br/> |xsd: string  <br/> |可选  <br/> ||Xsd: string 类型的值。  <br/> |
|Panose  <br/> |xsd: string  <br/> |可选  <br/> ||Xsd: string 类型的值。  <br/> |
|UnicodeRanges  <br/> |xsd: string  <br/> |可选  <br/> ||Xsd: string 类型的值。  <br/> |
   

