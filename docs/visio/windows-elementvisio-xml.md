---
title: Windows 元素 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: 包含文档的窗口元素。
ms.openlocfilehash: 70746ccfa2d99a9fdd5b3a91320c9372aa233c7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781657"
---
# <a name="windows-element-visio-xml"></a><span data-ttu-id="350e5-103">Windows 元素 (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="350e5-103">Windows element ('Visio XML')</span></span>

<span data-ttu-id="350e5-104">包含文档的**窗口**元素。</span><span class="sxs-lookup"><span data-stu-id="350e5-104">Contains the **Window** elements for a document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="350e5-105">元素信息</span><span class="sxs-lookup"><span data-stu-id="350e5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="350e5-106">**元素类型**</span><span class="sxs-lookup"><span data-stu-id="350e5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="350e5-107">Windows_Type</span><span class="sxs-lookup"><span data-stu-id="350e5-107">Windows_Type</span></span>](windows_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="350e5-108">**命名空间**</span><span class="sxs-lookup"><span data-stu-id="350e5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="350e5-109">**架构文件**</span><span class="sxs-lookup"><span data-stu-id="350e5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="350e5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="350e5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="350e5-111">**文档部件**</span><span class="sxs-lookup"><span data-stu-id="350e5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="350e5-112">windows.xml</span><span class="sxs-lookup"><span data-stu-id="350e5-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="350e5-113">定义</span><span class="sxs-lookup"><span data-stu-id="350e5-113">Definition</span></span>

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="350e5-114">元素和属性</span><span class="sxs-lookup"><span data-stu-id="350e5-114">Elements and attributes</span></span>

<span data-ttu-id="350e5-115">如果此架构定义了具体要求，如**sequence**， **minOccurs**、 **maxOccurs**和**choice**，请参阅定义部分。</span><span class="sxs-lookup"><span data-stu-id="350e5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="350e5-116">父元素</span><span class="sxs-lookup"><span data-stu-id="350e5-116">Parent elements</span></span>

<span data-ttu-id="350e5-117">无。</span><span class="sxs-lookup"><span data-stu-id="350e5-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="350e5-118">子元素</span><span class="sxs-lookup"><span data-stu-id="350e5-118">Child elements</span></span>

|<span data-ttu-id="350e5-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="350e5-119">**Element**</span></span>|<span data-ttu-id="350e5-120">**类型**</span><span class="sxs-lookup"><span data-stu-id="350e5-120">**Type**</span></span>|<span data-ttu-id="350e5-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="350e5-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="350e5-122">Window</span><span class="sxs-lookup"><span data-stu-id="350e5-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="350e5-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="350e5-123">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="350e5-124">代表 Microsoft Visio 实例中打开的窗口。</span><span class="sxs-lookup"><span data-stu-id="350e5-124">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="350e5-125">属性</span><span class="sxs-lookup"><span data-stu-id="350e5-125">Attributes</span></span>

|<span data-ttu-id="350e5-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="350e5-126">**Attribute**</span></span>|<span data-ttu-id="350e5-127">**类型**</span><span class="sxs-lookup"><span data-stu-id="350e5-127">**Type**</span></span>|<span data-ttu-id="350e5-128">**必需**</span><span class="sxs-lookup"><span data-stu-id="350e5-128">**Required**</span></span>|<span data-ttu-id="350e5-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="350e5-129">**Description**</span></span>|<span data-ttu-id="350e5-130">**可能的值**</span><span class="sxs-lookup"><span data-stu-id="350e5-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="350e5-131">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="350e5-131">ClientHeight</span></span>  <br/> |<span data-ttu-id="350e5-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="350e5-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="350e5-133">可选</span><span class="sxs-lookup"><span data-stu-id="350e5-133">optional</span></span>  <br/> |<span data-ttu-id="350e5-134">代表尺寸显示区域的高度</span><span class="sxs-lookup"><span data-stu-id="350e5-134">Represents the height dimension of a display area</span></span>  <br/> |<span data-ttu-id="350e5-135">Xsd:unsignedShort 类型的值。</span><span class="sxs-lookup"><span data-stu-id="350e5-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="350e5-136">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="350e5-136">ClientWidth</span></span>  <br/> |<span data-ttu-id="350e5-137">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="350e5-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="350e5-138">可选</span><span class="sxs-lookup"><span data-stu-id="350e5-138">optional</span></span>  <br/> |<span data-ttu-id="350e5-139">代表显示区域的宽度维度</span><span class="sxs-lookup"><span data-stu-id="350e5-139">Represents the width dimension of a display area</span></span>  <br/> |<span data-ttu-id="350e5-140">Xsd:unsignedShort 类型的值。</span><span class="sxs-lookup"><span data-stu-id="350e5-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   
