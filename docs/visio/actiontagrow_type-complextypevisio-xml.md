---
title: ActionTagRow_Type 复杂类型 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d42c212-b068-84fa-e271-bbe1fae52a48
ms.openlocfilehash: 810018ff98e430b01e07a4a6927a105c34336110
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19779626"
---
# <a name="actiontagrowtype-complextype-visio-xml"></a><span data-ttu-id="302d2-102">ActionTagRow_Type 复杂类型 (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="302d2-102">ActionTagRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="302d2-103">类型信息</span><span class="sxs-lookup"><span data-stu-id="302d2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="302d2-104">**命名空间**</span><span class="sxs-lookup"><span data-stu-id="302d2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="302d2-105">**架构文件**</span><span class="sxs-lookup"><span data-stu-id="302d2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="302d2-106">VisioSchema15 2012 06 05.xsd</span><span class="sxs-lookup"><span data-stu-id="302d2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="302d2-107">**扩展基**</span><span class="sxs-lookup"><span data-stu-id="302d2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="302d2-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="302d2-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="302d2-109">定义</span><span class="sxs-lookup"><span data-stu-id="302d2-109">Definition</span></span>

```XML
          <xs:complexType name="ActionTagRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="302d2-110">元素和属性</span><span class="sxs-lookup"><span data-stu-id="302d2-110">Elements and attributes</span></span>

<span data-ttu-id="302d2-111">如果此架构定义了具体要求，如**sequence**， **minOccurs**、 **maxOccurs**和**choice**，请参阅定义部分。</span><span class="sxs-lookup"><span data-stu-id="302d2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="302d2-112">子元素</span><span class="sxs-lookup"><span data-stu-id="302d2-112">Child elements</span></span>

|<span data-ttu-id="302d2-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="302d2-113">**Element**</span></span>|<span data-ttu-id="302d2-114">**类型**</span><span class="sxs-lookup"><span data-stu-id="302d2-114">**Type**</span></span>|<span data-ttu-id="302d2-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="302d2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="302d2-116">Cell</span><span class="sxs-lookup"><span data-stu-id="302d2-116">Cell</span></span>](cell-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="302d2-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="302d2-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="302d2-118">Attributes</span><span class="sxs-lookup"><span data-stu-id="302d2-118">Attributes</span></span>

<span data-ttu-id="302d2-119">无。</span><span class="sxs-lookup"><span data-stu-id="302d2-119">None.</span></span>
  
