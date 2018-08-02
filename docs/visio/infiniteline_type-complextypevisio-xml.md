---
title: InfiniteLine_Type 复杂类型 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4463d388-f5dd-4c43-71d4-82ba216d8d39
ms.openlocfilehash: 9e2b9146a875ecd32ccdc99e566a455aa36c2bf7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19780464"
---
# <a name="infinitelinetype-complextype-visio-xml"></a><span data-ttu-id="bb2b7-102">InfiniteLine_Type 复杂类型 (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="bb2b7-102">InfiniteLine_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bb2b7-103">类型信息</span><span class="sxs-lookup"><span data-stu-id="bb2b7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb2b7-104">**命名空间**</span><span class="sxs-lookup"><span data-stu-id="bb2b7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bb2b7-105">**架构文件**</span><span class="sxs-lookup"><span data-stu-id="bb2b7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bb2b7-106">VisioSchema15 2012 06 05.xsd</span><span class="sxs-lookup"><span data-stu-id="bb2b7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bb2b7-107">**扩展基**</span><span class="sxs-lookup"><span data-stu-id="bb2b7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bb2b7-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="bb2b7-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bb2b7-109">定义</span><span class="sxs-lookup"><span data-stu-id="bb2b7-109">Definition</span></span>

```XML
          <xs:complexType name="InfiniteLine_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bb2b7-110">元素和属性</span><span class="sxs-lookup"><span data-stu-id="bb2b7-110">Elements and attributes</span></span>

<span data-ttu-id="bb2b7-111">如果此架构定义了具体要求，如**sequence**， **minOccurs**、 **maxOccurs**和**choice**，请参阅定义部分。</span><span class="sxs-lookup"><span data-stu-id="bb2b7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bb2b7-112">子元素</span><span class="sxs-lookup"><span data-stu-id="bb2b7-112">Child elements</span></span>

|<span data-ttu-id="bb2b7-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="bb2b7-113">**Element**</span></span>|<span data-ttu-id="bb2b7-114">**类型**</span><span class="sxs-lookup"><span data-stu-id="bb2b7-114">**Type**</span></span>|<span data-ttu-id="bb2b7-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="bb2b7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bb2b7-116">Cell</span><span class="sxs-lookup"><span data-stu-id="bb2b7-116">Cell</span></span>](cell-element-infiniteline-rowvisio-xml.md) <br/> |[<span data-ttu-id="bb2b7-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="bb2b7-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bb2b7-118">Attributes</span><span class="sxs-lookup"><span data-stu-id="bb2b7-118">Attributes</span></span>

<span data-ttu-id="bb2b7-119">无。</span><span class="sxs-lookup"><span data-stu-id="bb2b7-119">None.</span></span>
  
