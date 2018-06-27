---
title: PidTagSpamThreshold 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2b2d6b8e-e3dd-4a9b-8bb5-53add675605d
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 24a033269b072712fea6e9957d0ffac3573ce3a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778419"
---
# <a name="pidtagspamthreshold-canonical-property"></a><span data-ttu-id="6c6d8-103">PidTagSpamThreshold 规范属性</span><span class="sxs-lookup"><span data-stu-id="6c6d8-103">PidTagSpamThreshold Canonical Property</span></span>

  
  
<span data-ttu-id="6c6d8-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="6c6d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6c6d8-105">Long 值，该值指示垃圾邮件筛选的级别。</span><span class="sxs-lookup"><span data-stu-id="6c6d8-105">A long value that indicates the level of spam filtering.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c6d8-106">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="6c6d8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c6d8-107">PR_SPAM_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="6c6d8-107">PR_SPAM_THRESHOLD</span></span>  <br/> |
|<span data-ttu-id="6c6d8-108">长 ID （盖）：</span><span class="sxs-lookup"><span data-stu-id="6c6d8-108">Long ID (LID):</span></span>  <br/> | <span data-ttu-id="6c6d8-109">0x041B</span><span class="sxs-lookup"><span data-stu-id="6c6d8-109">0x041B</span></span>  <br/> |
|<span data-ttu-id="6c6d8-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="6c6d8-110">Data type:</span></span>  <br/> |<span data-ttu-id="6c6d8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6c6d8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6c6d8-112">区域：</span><span class="sxs-lookup"><span data-stu-id="6c6d8-112">Area:</span></span>  <br/> |<span data-ttu-id="6c6d8-113">垃圾邮件</span><span class="sxs-lookup"><span data-stu-id="6c6d8-113">Spam</span></span>  <br/> |
   
## <a name="values"></a><span data-ttu-id="6c6d8-114">值</span><span class="sxs-lookup"><span data-stu-id="6c6d8-114">Values</span></span>

<span data-ttu-id="6c6d8-115">垃圾邮件筛选的值如下所示：</span><span class="sxs-lookup"><span data-stu-id="6c6d8-115">The values for spam filtering are as follows:</span></span>
  
|<span data-ttu-id="6c6d8-116">**垃圾邮件级别**</span><span class="sxs-lookup"><span data-stu-id="6c6d8-116">**Spam Level**</span></span>|<span data-ttu-id="6c6d8-117">**值**</span><span class="sxs-lookup"><span data-stu-id="6c6d8-117">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6c6d8-118">无</span><span class="sxs-lookup"><span data-stu-id="6c6d8-118">None</span></span>  <br/> |<span data-ttu-id="6c6d8-119">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="6c6d8-119">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="6c6d8-120">Low</span><span class="sxs-lookup"><span data-stu-id="6c6d8-120">Low</span></span>  <br/> |<span data-ttu-id="6c6d8-121">0x00000006</span><span class="sxs-lookup"><span data-stu-id="6c6d8-121">0x00000006</span></span>  <br/> |
|<span data-ttu-id="6c6d8-122">Medium</span><span class="sxs-lookup"><span data-stu-id="6c6d8-122">Medium</span></span>  <br/> |<span data-ttu-id="6c6d8-123">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6c6d8-123">0x00000005</span></span>  <br/> |
|<span data-ttu-id="6c6d8-124">High</span><span class="sxs-lookup"><span data-stu-id="6c6d8-124">High</span></span>  <br/> |<span data-ttu-id="6c6d8-125">0x00000003</span><span class="sxs-lookup"><span data-stu-id="6c6d8-125">0x00000003</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="6c6d8-126">相关资源</span><span class="sxs-lookup"><span data-stu-id="6c6d8-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c6d8-127">协议规范</span><span class="sxs-lookup"><span data-stu-id="6c6d8-127">Protocol specifications</span></span>

<span data-ttu-id="6c6d8-128">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c6d8-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c6d8-129">提供属性集定义和相关的 Microsoft Exchange Server 协议规范的引用。</span><span class="sxs-lookup"><span data-stu-id="6c6d8-129">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c6d8-130">[[MS OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c6d8-130">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c6d8-131">允许处理的允许/阻止列表，并确定的垃圾邮件。</span><span class="sxs-lookup"><span data-stu-id="6c6d8-131">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c6d8-132">头文件</span><span class="sxs-lookup"><span data-stu-id="6c6d8-132">Header files</span></span>

<span data-ttu-id="6c6d8-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c6d8-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c6d8-134">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="6c6d8-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="6c6d8-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6c6d8-135">Mapitags.h</span></span>
  
> <span data-ttu-id="6c6d8-136">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="6c6d8-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c6d8-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6c6d8-137">See also</span></span>



[<span data-ttu-id="6c6d8-138">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="6c6d8-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c6d8-139">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="6c6d8-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c6d8-140">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="6c6d8-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c6d8-141">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="6c6d8-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
