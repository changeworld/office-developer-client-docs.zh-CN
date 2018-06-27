---
title: PidTagToDoItemFlags 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagToDoItemFlags
api_type:
- COM
ms.assetid: bb7ccb45-ce08-4d22-9259-db15cd267e34
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: cae4ef6e4d7634ca2b429eb946aa948f5d90cd92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778541"
---
# <a name="pidtagtodoitemflags-canonical-property"></a><span data-ttu-id="ca270-103">PidTagToDoItemFlags 规范属性</span><span class="sxs-lookup"><span data-stu-id="ca270-103">PidTagToDoItemFlags Canonical Property</span></span>

  
  
<span data-ttu-id="ca270-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="ca270-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ca270-105">代表一个待办事项已标记的条件。</span><span class="sxs-lookup"><span data-stu-id="ca270-105">Represents a To-Do item's flagged condition.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca270-106">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="ca270-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ca270-107">PR_TODO_ITEM_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ca270-107">PR_TODO_ITEM_FLAGS</span></span>  <br/> |
|<span data-ttu-id="ca270-108">标识符:</span><span class="sxs-lookup"><span data-stu-id="ca270-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ca270-109">0x0E2B</span><span class="sxs-lookup"><span data-stu-id="ca270-109">0x0E2B</span></span>  <br/> |
|<span data-ttu-id="ca270-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="ca270-110">Data type:</span></span>  <br/> |<span data-ttu-id="ca270-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ca270-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ca270-112">区域：</span><span class="sxs-lookup"><span data-stu-id="ca270-112">Area:</span></span>  <br/> |<span data-ttu-id="ca270-113">MAPI 非可传送</span><span class="sxs-lookup"><span data-stu-id="ca270-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca270-114">备注</span><span class="sxs-lookup"><span data-stu-id="ca270-114">Remarks</span></span>

<span data-ttu-id="ca270-115">此属性是在其中的每个位应设置为 1 如果关联的条件下表中应用，否则为 0 位字段。</span><span class="sxs-lookup"><span data-stu-id="ca270-115">This property is a bit field in which each bit should be set to 1 if the associated condition in the following table applies, otherwise 0.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="ca270-116">数值</span><span class="sxs-lookup"><span data-stu-id="ca270-116">Numeric value</span></span>  <br/> |<span data-ttu-id="ca270-117">名称</span><span class="sxs-lookup"><span data-stu-id="ca270-117">Name</span></span>  <br/> |<span data-ttu-id="ca270-118">说明</span><span class="sxs-lookup"><span data-stu-id="ca270-118">Description</span></span>  <br/> |
|<span data-ttu-id="ca270-119">不存在</span><span class="sxs-lookup"><span data-stu-id="ca270-119">Not present</span></span>  <br/> |<span data-ttu-id="ca270-120">N/A</span><span class="sxs-lookup"><span data-stu-id="ca270-120">N/A</span></span>  <br/> |<span data-ttu-id="ca270-121">未标记</span><span class="sxs-lookup"><span data-stu-id="ca270-121">Unflagged</span></span>  <br/> |
|<span data-ttu-id="ca270-122">1</span><span class="sxs-lookup"><span data-stu-id="ca270-122">1</span></span>  <br/> |<span data-ttu-id="ca270-123">todoTimeFlagged</span><span class="sxs-lookup"><span data-stu-id="ca270-123">todoTimeFlagged</span></span>  <br/> |<span data-ttu-id="ca270-124">对象为标记的时间</span><span class="sxs-lookup"><span data-stu-id="ca270-124">Object is time flagged</span></span>  <br/> |
|<span data-ttu-id="ca270-125">8</span><span class="sxs-lookup"><span data-stu-id="ca270-125">8</span></span>  <br/> |<span data-ttu-id="ca270-126">todoRecipientFlagged</span><span class="sxs-lookup"><span data-stu-id="ca270-126">todoRecipientFlagged</span></span>  <br/> |<span data-ttu-id="ca270-127">只应在草稿 message 对象，设置和意味着对象进行了标记的收件人。</span><span class="sxs-lookup"><span data-stu-id="ca270-127">Should only be set on a draft message object, and it means that the object is flagged for recipients.</span></span>  <br/> |
   
<span data-ttu-id="ca270-128">保留所有未指定表中的位。</span><span class="sxs-lookup"><span data-stu-id="ca270-128">All bits that are not specified in the table are reserved.</span></span> <span data-ttu-id="ca270-129">它们必须被忽略，但如果已设置应保留。</span><span class="sxs-lookup"><span data-stu-id="ca270-129">They must be ignored, but should be preserved if they are set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ca270-130">相关资源</span><span class="sxs-lookup"><span data-stu-id="ca270-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ca270-131">协议规范</span><span class="sxs-lookup"><span data-stu-id="ca270-131">Protocol specifications</span></span>

<span data-ttu-id="ca270-132">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca270-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca270-133">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="ca270-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ca270-134">[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca270-134">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca270-135">指定的属性和与标记的操作。</span><span class="sxs-lookup"><span data-stu-id="ca270-135">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ca270-136">头文件</span><span class="sxs-lookup"><span data-stu-id="ca270-136">Header files</span></span>

<span data-ttu-id="ca270-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca270-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="ca270-138">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="ca270-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="ca270-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ca270-139">Mapitags.h</span></span>
  
> <span data-ttu-id="ca270-140">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="ca270-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca270-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ca270-141">See also</span></span>



[<span data-ttu-id="ca270-142">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="ca270-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ca270-143">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="ca270-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ca270-144">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="ca270-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ca270-145">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="ca270-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
