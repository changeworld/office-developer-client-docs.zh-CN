---
title: Scratch_Type 复杂类型 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e3dd8c8-e84c-61ff-bfff-57d97545e441
ms.openlocfilehash: 973a0db86eec553c7a728095e28735d4cdb91041
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781215"
---
# <a name="scratchtype-complextype-visio-xml"></a><span data-ttu-id="67dca-102">Scratch_Type 复杂类型 (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="67dca-102">Scratch_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="67dca-103">类型信息</span><span class="sxs-lookup"><span data-stu-id="67dca-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67dca-104">**命名空间**</span><span class="sxs-lookup"><span data-stu-id="67dca-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="67dca-105">**架构文件**</span><span class="sxs-lookup"><span data-stu-id="67dca-105">**Schema file**</span></span> <br/> |<span data-ttu-id="67dca-106">VisioSchema15 2012 06 05.xsd</span><span class="sxs-lookup"><span data-stu-id="67dca-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="67dca-107">**扩展基**</span><span class="sxs-lookup"><span data-stu-id="67dca-107">**Extension base**</span></span> <br/> |<span data-ttu-id="67dca-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="67dca-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="67dca-109">定义</span><span class="sxs-lookup"><span data-stu-id="67dca-109">Definition</span></span>

```XML
          <xs:complexType name="Scratch_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ScratchRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="67dca-110">元素和属性</span><span class="sxs-lookup"><span data-stu-id="67dca-110">Elements and attributes</span></span>

<span data-ttu-id="67dca-111">如果此架构定义了具体要求，如**sequence**， **minOccurs**、 **maxOccurs**和**choice**，请参阅定义部分。</span><span class="sxs-lookup"><span data-stu-id="67dca-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="67dca-112">子元素</span><span class="sxs-lookup"><span data-stu-id="67dca-112">Child elements</span></span>

|<span data-ttu-id="67dca-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="67dca-113">**Element**</span></span>|<span data-ttu-id="67dca-114">**类型**</span><span class="sxs-lookup"><span data-stu-id="67dca-114">**Type**</span></span>|<span data-ttu-id="67dca-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="67dca-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67dca-116">Row</span><span class="sxs-lookup"><span data-stu-id="67dca-116">Row</span></span>](row-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="67dca-117">ScratchRow_Type</span><span class="sxs-lookup"><span data-stu-id="67dca-117">ScratchRow_Type</span></span>](scratchrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="67dca-118">属性</span><span class="sxs-lookup"><span data-stu-id="67dca-118">Attributes</span></span>

<span data-ttu-id="67dca-119">无。</span><span class="sxs-lookup"><span data-stu-id="67dca-119">None.</span></span>
  
