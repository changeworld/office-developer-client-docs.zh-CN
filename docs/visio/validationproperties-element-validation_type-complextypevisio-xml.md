---
title: ValidationProperties 元素 （Validation_Type 复杂类型） (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a51a60c9-479b-7d7b-860f-bb46fc8b4d63
description: 封装与文档的验证相关的属性。
ms.openlocfilehash: 4f91160969cfb162f18440019ced23ea62061879
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781616"
---
# <a name="validationproperties-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="22b70-103">ValidationProperties 元素 （Validation_Type 复杂类型） (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="22b70-103">ValidationProperties element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="22b70-104">封装与文档的验证相关的属性。</span><span class="sxs-lookup"><span data-stu-id="22b70-104">Encapsulates the properties that are related to the document's validation.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22b70-105">元素信息</span><span class="sxs-lookup"><span data-stu-id="22b70-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22b70-106">**元素类型**</span><span class="sxs-lookup"><span data-stu-id="22b70-106">**Element type**</span></span> <br/> |[<span data-ttu-id="22b70-107">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="22b70-107">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="22b70-108">**命名空间**</span><span class="sxs-lookup"><span data-stu-id="22b70-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="22b70-109">**架构文件**</span><span class="sxs-lookup"><span data-stu-id="22b70-109">**Schema file**</span></span> <br/> |<span data-ttu-id="22b70-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="22b70-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="22b70-111">**文档部件**</span><span class="sxs-lookup"><span data-stu-id="22b70-111">**Document parts**</span></span> <br/> |<span data-ttu-id="22b70-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="22b70-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="22b70-113">定义</span><span class="sxs-lookup"><span data-stu-id="22b70-113">Definition</span></span>

```XML
< xs:element name="ValidationProperties" type="ValidationProperties_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="22b70-114">元素和属性</span><span class="sxs-lookup"><span data-stu-id="22b70-114">Elements and attributes</span></span>

<span data-ttu-id="22b70-115">如果此架构定义了具体要求，如**sequence**， **minOccurs**、 **maxOccurs**和**choice**，请参阅定义部分。</span><span class="sxs-lookup"><span data-stu-id="22b70-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="22b70-116">父元素</span><span class="sxs-lookup"><span data-stu-id="22b70-116">Parent elements</span></span>

|<span data-ttu-id="22b70-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="22b70-117">**Element**</span></span>|<span data-ttu-id="22b70-118">**类型**</span><span class="sxs-lookup"><span data-stu-id="22b70-118">**Type**</span></span>|<span data-ttu-id="22b70-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="22b70-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="22b70-120">验证</span><span class="sxs-lookup"><span data-stu-id="22b70-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="22b70-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="22b70-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="22b70-122">存储有关文档图表验证的信息。</span><span class="sxs-lookup"><span data-stu-id="22b70-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="22b70-123">子元素</span><span class="sxs-lookup"><span data-stu-id="22b70-123">Child elements</span></span>

<span data-ttu-id="22b70-124">无。</span><span class="sxs-lookup"><span data-stu-id="22b70-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22b70-125">属性</span><span class="sxs-lookup"><span data-stu-id="22b70-125">Attributes</span></span>

|<span data-ttu-id="22b70-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="22b70-126">**Attribute**</span></span>|<span data-ttu-id="22b70-127">**类型**</span><span class="sxs-lookup"><span data-stu-id="22b70-127">**Type**</span></span>|<span data-ttu-id="22b70-128">**必需**</span><span class="sxs-lookup"><span data-stu-id="22b70-128">**Required**</span></span>|<span data-ttu-id="22b70-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="22b70-129">**Description**</span></span>|<span data-ttu-id="22b70-130">**可能的值**</span><span class="sxs-lookup"><span data-stu-id="22b70-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="22b70-131">LastValidated</span><span class="sxs-lookup"><span data-stu-id="22b70-131">LastValidated</span></span>  <br/> |<span data-ttu-id="22b70-132">化</span><span class="sxs-lookup"><span data-stu-id="22b70-132">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="22b70-133">必需</span><span class="sxs-lookup"><span data-stu-id="22b70-133">required</span></span>  <br/> |<span data-ttu-id="22b70-134">日期和时间的上次验证文档。</span><span class="sxs-lookup"><span data-stu-id="22b70-134">The date and time that the document was last validated.</span></span>  <br/> |<span data-ttu-id="22b70-135">化类型的值。</span><span class="sxs-lookup"><span data-stu-id="22b70-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="22b70-136">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="22b70-136">ShowIgnored</span></span>  <br/> |<span data-ttu-id="22b70-137">化</span><span class="sxs-lookup"><span data-stu-id="22b70-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="22b70-138">必需</span><span class="sxs-lookup"><span data-stu-id="22b70-138">required</span></span>  <br/> |<span data-ttu-id="22b70-139">指定是否在问题窗口中显示忽略的验证问题。</span><span class="sxs-lookup"><span data-stu-id="22b70-139">Specifies whether to show ignored validation issues in the Issues window.</span></span>  <br/> |<span data-ttu-id="22b70-140">化类型的值。</span><span class="sxs-lookup"><span data-stu-id="22b70-140">Values of the xsd:boolean type.</span></span>  <br/> |
   
