---
title: SectionDef_Type 复杂类型 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: 426e62ea7a9f990555776e3ac732dd43e614582d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781231"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="db129-102">SectionDef_Type 复杂类型 (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="db129-102">SectionDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="db129-103">类型信息</span><span class="sxs-lookup"><span data-stu-id="db129-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db129-104">**命名空间**</span><span class="sxs-lookup"><span data-stu-id="db129-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="db129-105">**架构文件**</span><span class="sxs-lookup"><span data-stu-id="db129-105">**Schema file**</span></span> <br/> |<span data-ttu-id="db129-106">VisioSchema15 2012 06 05.xsd</span><span class="sxs-lookup"><span data-stu-id="db129-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="db129-107">**扩展基**</span><span class="sxs-lookup"><span data-stu-id="db129-107">**Extension base**</span></span> <br/> |<span data-ttu-id="db129-108">无</span><span class="sxs-lookup"><span data-stu-id="db129-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="db129-109">定义</span><span class="sxs-lookup"><span data-stu-id="db129-109">Definition</span></span>

```XML
          <xs:complexType name="SectionDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowDef"  type="RowDef_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="db129-110">元素和属性</span><span class="sxs-lookup"><span data-stu-id="db129-110">Elements and attributes</span></span>

<span data-ttu-id="db129-111">如果此架构定义了具体要求，如**sequence**， **minOccurs**、 **maxOccurs**和**choice**，请参阅定义部分。</span><span class="sxs-lookup"><span data-stu-id="db129-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="db129-112">子元素</span><span class="sxs-lookup"><span data-stu-id="db129-112">Child elements</span></span>

|<span data-ttu-id="db129-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="db129-113">**Element**</span></span>|<span data-ttu-id="db129-114">**类型**</span><span class="sxs-lookup"><span data-stu-id="db129-114">**Type**</span></span>|<span data-ttu-id="db129-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="db129-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="db129-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="db129-116">CellDef</span></span>](http://msdn.microsoft.com/library/f0ec7afe-9e0a-b5e5-82dd-4adff1c1607f%28Office.15%29.aspx) <br/> |[<span data-ttu-id="db129-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="db129-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="db129-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="db129-118">RowDef</span></span>](http://msdn.microsoft.com/library/25615be9-1d19-1ba9-4192-7d4a0dfae717%28Office.15%29.aspx) <br/> |[<span data-ttu-id="db129-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="db129-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="db129-120">属性</span><span class="sxs-lookup"><span data-stu-id="db129-120">Attributes</span></span>

|<span data-ttu-id="db129-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="db129-121">**Attribute**</span></span>|<span data-ttu-id="db129-122">**类型**</span><span class="sxs-lookup"><span data-stu-id="db129-122">**Type**</span></span>|<span data-ttu-id="db129-123">**必需**</span><span class="sxs-lookup"><span data-stu-id="db129-123">**Required**</span></span>|<span data-ttu-id="db129-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="db129-124">**Description**</span></span>|<span data-ttu-id="db129-125">**可能的值**</span><span class="sxs-lookup"><span data-stu-id="db129-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="db129-126">N</span><span class="sxs-lookup"><span data-stu-id="db129-126">N</span></span>  <br/> |<span data-ttu-id="db129-127">xsd: string</span><span class="sxs-lookup"><span data-stu-id="db129-127">xsd:string</span></span>  <br/> |<span data-ttu-id="db129-128">必需</span><span class="sxs-lookup"><span data-stu-id="db129-128">required</span></span>  <br/> ||<span data-ttu-id="db129-129">Xsd: string 类型的值。</span><span class="sxs-lookup"><span data-stu-id="db129-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="db129-130">S</span><span class="sxs-lookup"><span data-stu-id="db129-130">S</span></span>  <br/> |<span data-ttu-id="db129-131">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="db129-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="db129-132">可选</span><span class="sxs-lookup"><span data-stu-id="db129-132">optional</span></span>  <br/> ||<span data-ttu-id="db129-133">Xsd:unsignedByte 类型的值。</span><span class="sxs-lookup"><span data-stu-id="db129-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="db129-134">T</span><span class="sxs-lookup"><span data-stu-id="db129-134">T</span></span>  <br/> |<span data-ttu-id="db129-135">xsd: string</span><span class="sxs-lookup"><span data-stu-id="db129-135">xsd:string</span></span>  <br/> |<span data-ttu-id="db129-136">可选</span><span class="sxs-lookup"><span data-stu-id="db129-136">optional</span></span>  <br/> ||<span data-ttu-id="db129-137">Xsd: string 类型的值。</span><span class="sxs-lookup"><span data-stu-id="db129-137">Values of the xsd:string type.</span></span>  <br/> |
   
