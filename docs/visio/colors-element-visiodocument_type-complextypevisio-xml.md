---
title: Colors 元素 （VisioDocument_Type 复杂类型） (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: 包含文档颜色表。
ms.openlocfilehash: d13690ce6e1772ab1a43e697e8b99c0776a204b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19779898"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="9fb2d-103">Colors 元素 （VisioDocument_Type 复杂类型） (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9fb2d-103">Colors element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9fb2d-104">包含文档颜色表。</span><span class="sxs-lookup"><span data-stu-id="9fb2d-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9fb2d-105">元素信息</span><span class="sxs-lookup"><span data-stu-id="9fb2d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fb2d-106">**元素类型**</span><span class="sxs-lookup"><span data-stu-id="9fb2d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9fb2d-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="9fb2d-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9fb2d-108">**命名空间**</span><span class="sxs-lookup"><span data-stu-id="9fb2d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9fb2d-109">**架构文件**</span><span class="sxs-lookup"><span data-stu-id="9fb2d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9fb2d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9fb2d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9fb2d-111">**文档部件**</span><span class="sxs-lookup"><span data-stu-id="9fb2d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9fb2d-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="9fb2d-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9fb2d-113">定义</span><span class="sxs-lookup"><span data-stu-id="9fb2d-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9fb2d-114">元素和属性</span><span class="sxs-lookup"><span data-stu-id="9fb2d-114">Elements and attributes</span></span>

<span data-ttu-id="9fb2d-115">如果此架构定义了具体要求，如**sequence**， **minOccurs**、 **maxOccurs**和**choice**，请参阅定义部分。</span><span class="sxs-lookup"><span data-stu-id="9fb2d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9fb2d-116">父元素</span><span class="sxs-lookup"><span data-stu-id="9fb2d-116">Parent elements</span></span>

|<span data-ttu-id="9fb2d-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="9fb2d-117">**Element**</span></span>|<span data-ttu-id="9fb2d-118">**类型**</span><span class="sxs-lookup"><span data-stu-id="9fb2d-118">**Type**</span></span>|<span data-ttu-id="9fb2d-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="9fb2d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9fb2d-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="9fb2d-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="9fb2d-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="9fb2d-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9fb2d-122">Microsoft Visio 文档的根元素。</span><span class="sxs-lookup"><span data-stu-id="9fb2d-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9fb2d-123">子元素</span><span class="sxs-lookup"><span data-stu-id="9fb2d-123">Child elements</span></span>

|<span data-ttu-id="9fb2d-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="9fb2d-124">**Element**</span></span>|<span data-ttu-id="9fb2d-125">**类型**</span><span class="sxs-lookup"><span data-stu-id="9fb2d-125">**Type**</span></span>|<span data-ttu-id="9fb2d-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="9fb2d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9fb2d-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="9fb2d-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fb2d-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="9fb2d-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9fb2d-129">包含颜色表项。</span><span class="sxs-lookup"><span data-stu-id="9fb2d-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9fb2d-130">属性</span><span class="sxs-lookup"><span data-stu-id="9fb2d-130">Attributes</span></span>

<span data-ttu-id="9fb2d-131">无。</span><span class="sxs-lookup"><span data-stu-id="9fb2d-131">None.</span></span>
  
