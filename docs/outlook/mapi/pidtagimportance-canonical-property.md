---
title: PidTagImportance 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 9f6a67dcff6c74f44bbc64ae8b95f3e0ec284a90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19777721"
---
# <a name="pidtagimportance-canonical-property"></a><span data-ttu-id="b8236-103">PidTagImportance 规范属性</span><span class="sxs-lookup"><span data-stu-id="b8236-103">PidTagImportance Canonical Property</span></span>

  
  
<span data-ttu-id="b8236-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="b8236-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b8236-105">包含一个值，指示邮件发件人的邮件的重要性的平均意见。</span><span class="sxs-lookup"><span data-stu-id="b8236-105">Contains a value that indicates the message sender's opinion of the importance of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b8236-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="b8236-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b8236-107">PR_IMPORTANCE</span><span class="sxs-lookup"><span data-stu-id="b8236-107">PR_IMPORTANCE</span></span>  <br/> |
|<span data-ttu-id="b8236-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="b8236-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b8236-109">0x0017</span><span class="sxs-lookup"><span data-stu-id="b8236-109">0x0017</span></span>  <br/> |
|<span data-ttu-id="b8236-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="b8236-110">Data type:</span></span>  <br/> |<span data-ttu-id="b8236-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b8236-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b8236-112">区域：</span><span class="sxs-lookup"><span data-stu-id="b8236-112">Area:</span></span>  <br/> |<span data-ttu-id="b8236-113">常规消息</span><span class="sxs-lookup"><span data-stu-id="b8236-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8236-114">说明</span><span class="sxs-lookup"><span data-stu-id="b8236-114">Remarks</span></span>

<span data-ttu-id="b8236-115">此属性和**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) 属性不能混淆。</span><span class="sxs-lookup"><span data-stu-id="b8236-115">This property and the **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="b8236-116">重要性表示到用户的值，而优先级表示订单设计 サ 频率邮件应发送的消息的系统软件的速度。</span><span class="sxs-lookup"><span data-stu-id="b8236-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="b8236-117">更高的优先级通常指示较高的开销。</span><span class="sxs-lookup"><span data-stu-id="b8236-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="b8236-118">更高重要性通常是与用户界面的不同显示相关联。</span><span class="sxs-lookup"><span data-stu-id="b8236-118">Higher importance usually is associated with a different display by the user interface.</span></span> 
  
<span data-ttu-id="b8236-119">此属性可以具有完全下列值之一：</span><span class="sxs-lookup"><span data-stu-id="b8236-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="b8236-120">IMPORTANCE_LOW</span><span class="sxs-lookup"><span data-stu-id="b8236-120">IMPORTANCE_LOW</span></span> 
  
> <span data-ttu-id="b8236-121">邮件已低重要性。</span><span class="sxs-lookup"><span data-stu-id="b8236-121">The message has low importance.</span></span>
    
<span data-ttu-id="b8236-122">IMPORTANCE_HIGH</span><span class="sxs-lookup"><span data-stu-id="b8236-122">IMPORTANCE_HIGH</span></span> 
  
> <span data-ttu-id="b8236-123">邮件已重要性-高。</span><span class="sxs-lookup"><span data-stu-id="b8236-123">The message has high importance.</span></span>
    
<span data-ttu-id="b8236-124">IMPORTANCE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="b8236-124">IMPORTANCE_NORMAL</span></span> 
  
> <span data-ttu-id="b8236-125">邮件具有普通重要性。</span><span class="sxs-lookup"><span data-stu-id="b8236-125">The message has normal importance.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="b8236-126">相关资源</span><span class="sxs-lookup"><span data-stu-id="b8236-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b8236-127">协议规范</span><span class="sxs-lookup"><span data-stu-id="b8236-127">Protocol specifications</span></span>

<span data-ttu-id="b8236-128">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8236-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8236-129">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="b8236-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b8236-130">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8236-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8236-131">处理邮件和附件的对象。</span><span class="sxs-lookup"><span data-stu-id="b8236-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b8236-132">头文件</span><span class="sxs-lookup"><span data-stu-id="b8236-132">Header files</span></span>

<span data-ttu-id="b8236-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b8236-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="b8236-134">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="b8236-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="b8236-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b8236-135">Mapitags.h</span></span>
  
> <span data-ttu-id="b8236-136">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="b8236-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b8236-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b8236-137">See also</span></span>



[<span data-ttu-id="b8236-138">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="b8236-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b8236-139">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="b8236-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b8236-140">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="b8236-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b8236-141">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="b8236-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
