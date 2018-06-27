---
title: Rule_Type 复杂类型 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: 380c59d659c820f0c5452ce37fa3616e1408a86c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781191"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="4f81f-102">Rule_Type 复杂类型 (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4f81f-102">Rule_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4f81f-103">类型信息</span><span class="sxs-lookup"><span data-stu-id="4f81f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f81f-104">**命名空间**</span><span class="sxs-lookup"><span data-stu-id="4f81f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4f81f-105">**架构文件**</span><span class="sxs-lookup"><span data-stu-id="4f81f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4f81f-106">VisioSchema15 2012 06 05.xsd</span><span class="sxs-lookup"><span data-stu-id="4f81f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4f81f-107">**扩展基**</span><span class="sxs-lookup"><span data-stu-id="4f81f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4f81f-108">无</span><span class="sxs-lookup"><span data-stu-id="4f81f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4f81f-109">定义</span><span class="sxs-lookup"><span data-stu-id="4f81f-109">Definition</span></span>

```XML
          <xs:complexType name="Rule_Type">
          
          <xs:sequence>
    <xs:element name="RuleFilter"  type="RuleFilter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleTest"  type="RuleTest_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Category"
  type="xsd:string"
    />
    <xs:attribute name="Description"
  type="xsd:string"
    />
    <xs:attribute name="RuleTarget"
  type="xsd:int"
    />
    <xs:attribute name="Ignored"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4f81f-110">元素和属性</span><span class="sxs-lookup"><span data-stu-id="4f81f-110">Elements and attributes</span></span>

<span data-ttu-id="4f81f-111">如果此架构定义了具体要求，如**sequence**， **minOccurs**、 **maxOccurs**和**choice**，请参阅定义部分。</span><span class="sxs-lookup"><span data-stu-id="4f81f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4f81f-112">子元素</span><span class="sxs-lookup"><span data-stu-id="4f81f-112">Child elements</span></span>

|<span data-ttu-id="4f81f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="4f81f-113">**Element**</span></span>|<span data-ttu-id="4f81f-114">**类型**</span><span class="sxs-lookup"><span data-stu-id="4f81f-114">**Type**</span></span>|<span data-ttu-id="4f81f-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="4f81f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4f81f-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="4f81f-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4f81f-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="4f81f-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4f81f-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="4f81f-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4f81f-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="4f81f-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4f81f-120">属性</span><span class="sxs-lookup"><span data-stu-id="4f81f-120">Attributes</span></span>

|<span data-ttu-id="4f81f-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="4f81f-121">**Attribute**</span></span>|<span data-ttu-id="4f81f-122">**类型**</span><span class="sxs-lookup"><span data-stu-id="4f81f-122">**Type**</span></span>|<span data-ttu-id="4f81f-123">**必需**</span><span class="sxs-lookup"><span data-stu-id="4f81f-123">**Required**</span></span>|<span data-ttu-id="4f81f-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="4f81f-124">**Description**</span></span>|<span data-ttu-id="4f81f-125">**可能的值**</span><span class="sxs-lookup"><span data-stu-id="4f81f-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4f81f-126">Category</span><span class="sxs-lookup"><span data-stu-id="4f81f-126">Category</span></span>  <br/> |<span data-ttu-id="4f81f-127">xsd: string</span><span class="sxs-lookup"><span data-stu-id="4f81f-127">xsd:string</span></span>  <br/> |<span data-ttu-id="4f81f-128">可选</span><span class="sxs-lookup"><span data-stu-id="4f81f-128">optional</span></span>  <br/> ||<span data-ttu-id="4f81f-129">Xsd: string 类型的值。</span><span class="sxs-lookup"><span data-stu-id="4f81f-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4f81f-130">说明</span><span class="sxs-lookup"><span data-stu-id="4f81f-130">Description</span></span>  <br/> |<span data-ttu-id="4f81f-131">xsd: string</span><span class="sxs-lookup"><span data-stu-id="4f81f-131">xsd:string</span></span>  <br/> |<span data-ttu-id="4f81f-132">可选</span><span class="sxs-lookup"><span data-stu-id="4f81f-132">optional</span></span>  <br/> ||<span data-ttu-id="4f81f-133">Xsd: string 类型的值。</span><span class="sxs-lookup"><span data-stu-id="4f81f-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4f81f-134">ID</span><span class="sxs-lookup"><span data-stu-id="4f81f-134">ID</span></span>  <br/> |<span data-ttu-id="4f81f-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4f81f-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4f81f-136">必需</span><span class="sxs-lookup"><span data-stu-id="4f81f-136">required</span></span>  <br/> ||<span data-ttu-id="4f81f-137">Xsd:unsignedInt 类型的值。</span><span class="sxs-lookup"><span data-stu-id="4f81f-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4f81f-138">忽略</span><span class="sxs-lookup"><span data-stu-id="4f81f-138">Ignored</span></span>  <br/> |<span data-ttu-id="4f81f-139">化</span><span class="sxs-lookup"><span data-stu-id="4f81f-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4f81f-140">可选</span><span class="sxs-lookup"><span data-stu-id="4f81f-140">optional</span></span>  <br/> ||<span data-ttu-id="4f81f-141">化类型的值。</span><span class="sxs-lookup"><span data-stu-id="4f81f-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4f81f-142">NameU</span><span class="sxs-lookup"><span data-stu-id="4f81f-142">NameU</span></span>  <br/> |<span data-ttu-id="4f81f-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="4f81f-143">xsd:string</span></span>  <br/> |<span data-ttu-id="4f81f-144">必需</span><span class="sxs-lookup"><span data-stu-id="4f81f-144">required</span></span>  <br/> ||<span data-ttu-id="4f81f-145">Xsd: string 类型的值。</span><span class="sxs-lookup"><span data-stu-id="4f81f-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4f81f-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="4f81f-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="4f81f-147">xsd:int</span><span class="sxs-lookup"><span data-stu-id="4f81f-147">xsd:int</span></span>  <br/> |<span data-ttu-id="4f81f-148">可选</span><span class="sxs-lookup"><span data-stu-id="4f81f-148">optional</span></span>  <br/> ||<span data-ttu-id="4f81f-149">Xsd:int 类型的值。</span><span class="sxs-lookup"><span data-stu-id="4f81f-149">Values of the xsd:int type.</span></span>  <br/> |
   
