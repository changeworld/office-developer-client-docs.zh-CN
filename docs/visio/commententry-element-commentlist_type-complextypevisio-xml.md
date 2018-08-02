---
title: CommentEntry 元素 （CommentList_Type 复杂类型） (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: 指定用于标识与绘图中的注释的属性。
ms.openlocfilehash: b2ab1925c8b3b9a9c2d67ac48c1db1768f5916b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19779912"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a><span data-ttu-id="8e657-103">CommentEntry 元素 （CommentList_Type 复杂类型） (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8e657-103">CommentEntry element (CommentList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8e657-104">指定用于标识与绘图中的注释的属性。</span><span class="sxs-lookup"><span data-stu-id="8e657-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8e657-105">元素信息</span><span class="sxs-lookup"><span data-stu-id="8e657-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e657-106">**元素类型**</span><span class="sxs-lookup"><span data-stu-id="8e657-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8e657-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="8e657-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8e657-108">**命名空间**</span><span class="sxs-lookup"><span data-stu-id="8e657-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8e657-109">**架构文件**</span><span class="sxs-lookup"><span data-stu-id="8e657-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8e657-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8e657-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8e657-111">**文档部件**</span><span class="sxs-lookup"><span data-stu-id="8e657-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8e657-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="8e657-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8e657-113">定义</span><span class="sxs-lookup"><span data-stu-id="8e657-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8e657-114">元素和属性</span><span class="sxs-lookup"><span data-stu-id="8e657-114">Elements and attributes</span></span>

<span data-ttu-id="8e657-115">如果此架构定义了具体要求，如**sequence**， **minOccurs**、 **maxOccurs**和**choice**，请参阅定义部分。</span><span class="sxs-lookup"><span data-stu-id="8e657-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8e657-116">父元素</span><span class="sxs-lookup"><span data-stu-id="8e657-116">Parent elements</span></span>

|<span data-ttu-id="8e657-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="8e657-117">**Element**</span></span>|<span data-ttu-id="8e657-118">**类型**</span><span class="sxs-lookup"><span data-stu-id="8e657-118">**Type**</span></span>|<span data-ttu-id="8e657-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="8e657-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8e657-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="8e657-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8e657-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="8e657-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8e657-122">指定与绘图中的注释。</span><span class="sxs-lookup"><span data-stu-id="8e657-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8e657-123">子元素</span><span class="sxs-lookup"><span data-stu-id="8e657-123">Child elements</span></span>

<span data-ttu-id="8e657-124">无。</span><span class="sxs-lookup"><span data-stu-id="8e657-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8e657-125">属性</span><span class="sxs-lookup"><span data-stu-id="8e657-125">Attributes</span></span>

|<span data-ttu-id="8e657-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="8e657-126">**Attribute**</span></span>|<span data-ttu-id="8e657-127">**类型**</span><span class="sxs-lookup"><span data-stu-id="8e657-127">**Type**</span></span>|<span data-ttu-id="8e657-128">**必需**</span><span class="sxs-lookup"><span data-stu-id="8e657-128">**Required**</span></span>|<span data-ttu-id="8e657-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="8e657-129">**Description**</span></span>|<span data-ttu-id="8e657-130">**可能的值**</span><span class="sxs-lookup"><span data-stu-id="8e657-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8e657-131">作者 Id</span><span class="sxs-lookup"><span data-stu-id="8e657-131">AuthorID</span></span>  <br/> |<span data-ttu-id="8e657-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8e657-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8e657-133">必需</span><span class="sxs-lookup"><span data-stu-id="8e657-133">required</span></span>  <br/> |<span data-ttu-id="8e657-134">一个从 1 开始的值，标识作者。</span><span class="sxs-lookup"><span data-stu-id="8e657-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="8e657-135">Xsd:unsignedInt 类型的值。</span><span class="sxs-lookup"><span data-stu-id="8e657-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8e657-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="8e657-136">CommentID</span></span>  <br/> |<span data-ttu-id="8e657-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8e657-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8e657-138">必需</span><span class="sxs-lookup"><span data-stu-id="8e657-138">required</span></span>  <br/> |<span data-ttu-id="8e657-139">一个唯一值，该值标识绘图页中的注释。</span><span class="sxs-lookup"><span data-stu-id="8e657-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="8e657-140">Xsd:unsignedInt 类型的值。</span><span class="sxs-lookup"><span data-stu-id="8e657-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8e657-141">Date</span><span class="sxs-lookup"><span data-stu-id="8e657-141">Date</span></span>  <br/> |<span data-ttu-id="8e657-142">化</span><span class="sxs-lookup"><span data-stu-id="8e657-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="8e657-143">必需</span><span class="sxs-lookup"><span data-stu-id="8e657-143">required</span></span>  <br/> |<span data-ttu-id="8e657-144">指定何时创建批注。</span><span class="sxs-lookup"><span data-stu-id="8e657-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="8e657-145">化类型的值。</span><span class="sxs-lookup"><span data-stu-id="8e657-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="8e657-146">完成</span><span class="sxs-lookup"><span data-stu-id="8e657-146">Done</span></span>  <br/> |<span data-ttu-id="8e657-147">化</span><span class="sxs-lookup"><span data-stu-id="8e657-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8e657-148">可选</span><span class="sxs-lookup"><span data-stu-id="8e657-148">optional</span></span>  <br/> |<span data-ttu-id="8e657-149">指定批注的当前状态。</span><span class="sxs-lookup"><span data-stu-id="8e657-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="8e657-150">化类型的值。</span><span class="sxs-lookup"><span data-stu-id="8e657-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8e657-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="8e657-151">EditDate</span></span>  <br/> |<span data-ttu-id="8e657-152">化</span><span class="sxs-lookup"><span data-stu-id="8e657-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="8e657-153">可选</span><span class="sxs-lookup"><span data-stu-id="8e657-153">optional</span></span>  <br/> |<span data-ttu-id="8e657-154">指定上次更改注释。</span><span class="sxs-lookup"><span data-stu-id="8e657-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="8e657-155">化类型的值。</span><span class="sxs-lookup"><span data-stu-id="8e657-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="8e657-156">PageID</span><span class="sxs-lookup"><span data-stu-id="8e657-156">PageID</span></span>  <br/> |<span data-ttu-id="8e657-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8e657-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8e657-158">必需</span><span class="sxs-lookup"><span data-stu-id="8e657-158">required</span></span>  <br/> |<span data-ttu-id="8e657-159">一个值，标识在绘图页上是注释。</span><span class="sxs-lookup"><span data-stu-id="8e657-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="8e657-160">Xsd:unsignedInt 类型的值。</span><span class="sxs-lookup"><span data-stu-id="8e657-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8e657-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="8e657-161">ShapeID</span></span>  <br/> |<span data-ttu-id="8e657-162">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8e657-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8e657-163">可选</span><span class="sxs-lookup"><span data-stu-id="8e657-163">optional</span></span>  <br/> |<span data-ttu-id="8e657-164">一个值，标识形状上是注释。</span><span class="sxs-lookup"><span data-stu-id="8e657-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="8e657-165">如果未不指定任何 ShapeID，批注引用绘图页。</span><span class="sxs-lookup"><span data-stu-id="8e657-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="8e657-166">Xsd:unsignedInt 类型的值。</span><span class="sxs-lookup"><span data-stu-id="8e657-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   
