---
title: PidTagSensitivity 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSensitivity
api_type:
- COM
ms.assetid: 5b678475-f2a8-4831-ad68-11654e09c821
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 93be3351749ac3e9d285fb214f746d58b55fb5b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778390"
---
# <a name="pidtagsensitivity-canonical-property"></a><span data-ttu-id="b878d-103">PidTagSensitivity 规范属性</span><span class="sxs-lookup"><span data-stu-id="b878d-103">PidTagSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="b878d-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="b878d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b878d-105">包含一个值，指示邮件发件人的邮件的敏感度的平均意见。</span><span class="sxs-lookup"><span data-stu-id="b878d-105">Contains a value that indicates the message sender's opinion of the sensitivity of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b878d-106">相关属性：</span><span class="sxs-lookup"><span data-stu-id="b878d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b878d-107">PR_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="b878d-107">PR_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="b878d-108">标识符：</span><span class="sxs-lookup"><span data-stu-id="b878d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b878d-109">0x0036</span><span class="sxs-lookup"><span data-stu-id="b878d-109">0x0036</span></span>  <br/> |
|<span data-ttu-id="b878d-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="b878d-110">Data type:</span></span>  <br/> |<span data-ttu-id="b878d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b878d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b878d-112">区域：</span><span class="sxs-lookup"><span data-stu-id="b878d-112">Area:</span></span>  <br/> |<span data-ttu-id="b878d-113">常规消息</span><span class="sxs-lookup"><span data-stu-id="b878d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b878d-114">说明</span><span class="sxs-lookup"><span data-stu-id="b878d-114">Remarks</span></span>

<span data-ttu-id="b878d-115">建议消息对象公开此属性。</span><span class="sxs-lookup"><span data-stu-id="b878d-115">It is recommended that message objects expose this property.</span></span>
  
<span data-ttu-id="b878d-116">此属性可以具有完全下列值之一：</span><span class="sxs-lookup"><span data-stu-id="b878d-116">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="b878d-117">SENSITIVITY_NONE</span><span class="sxs-lookup"><span data-stu-id="b878d-117">SENSITIVITY_NONE</span></span> 
  
> <span data-ttu-id="b878d-118">邮件有任何特殊的敏感度。</span><span class="sxs-lookup"><span data-stu-id="b878d-118">The message has no special sensitivity.</span></span>
    
<span data-ttu-id="b878d-119">SENSITIVITY_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="b878d-119">SENSITIVITY_PERSONAL</span></span> 
  
> <span data-ttu-id="b878d-120">消息为个人。</span><span class="sxs-lookup"><span data-stu-id="b878d-120">The message is personal.</span></span>
    
<span data-ttu-id="b878d-121">SENSITIVITY_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="b878d-121">SENSITIVITY_PRIVATE</span></span> 
  
> <span data-ttu-id="b878d-122">邮件是专用的。</span><span class="sxs-lookup"><span data-stu-id="b878d-122">The message is private.</span></span>
    
<span data-ttu-id="b878d-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span><span class="sxs-lookup"><span data-stu-id="b878d-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span></span> 
  
> <span data-ttu-id="b878d-124">邮件被指定公司机密。</span><span class="sxs-lookup"><span data-stu-id="b878d-124">The message is designated company confidential.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="b878d-125">相关资源</span><span class="sxs-lookup"><span data-stu-id="b878d-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b878d-126">协议规范</span><span class="sxs-lookup"><span data-stu-id="b878d-126">Protocol specifications</span></span>

<span data-ttu-id="b878d-127">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b878d-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b878d-128">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="b878d-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b878d-129">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b878d-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b878d-130">处理邮件和附件的对象。</span><span class="sxs-lookup"><span data-stu-id="b878d-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b878d-131">头文件</span><span class="sxs-lookup"><span data-stu-id="b878d-131">Header files</span></span>

<span data-ttu-id="b878d-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b878d-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="b878d-133">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="b878d-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="b878d-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b878d-134">Mapitags.h</span></span>
  
> <span data-ttu-id="b878d-135">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="b878d-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b878d-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b878d-136">See also</span></span>



[<span data-ttu-id="b878d-137">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="b878d-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b878d-138">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="b878d-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b878d-139">将规范属性名称映射到 MAPI 名称</span><span class="sxs-lookup"><span data-stu-id="b878d-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b878d-140">将 MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="b878d-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
