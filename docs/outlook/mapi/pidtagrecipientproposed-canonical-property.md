---
title: PidTagRecipientProposed 规范属性
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposed
api_type:
- COM
ms.assetid: 8cb0e46c-0937-482f-be78-1f2e5261b210
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 3b05f33328e9e0b90251a99defa9816f86971337
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19778152"
---
# <a name="pidtagrecipientproposed-canonical-property"></a><span data-ttu-id="690ae-103">PidTagRecipientProposed 规范属性</span><span class="sxs-lookup"><span data-stu-id="690ae-103">PidTagRecipientProposed Canonical Property</span></span>

  
  
<span data-ttu-id="690ae-104">**适用于**： Outlook</span><span class="sxs-lookup"><span data-stu-id="690ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="690ae-105">指示是否已经响应会议与会者。</span><span class="sxs-lookup"><span data-stu-id="690ae-105">Indicates whether a meeting attendee has responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="690ae-106">关联的属性：</span><span class="sxs-lookup"><span data-stu-id="690ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="690ae-107">PR_RECIPIENT_PROPOSED</span><span class="sxs-lookup"><span data-stu-id="690ae-107">PR_RECIPIENT_PROPOSED</span></span>  <br/> |
|<span data-ttu-id="690ae-108">标识符:</span><span class="sxs-lookup"><span data-stu-id="690ae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="690ae-109">0x5FE1</span><span class="sxs-lookup"><span data-stu-id="690ae-109">0x5FE1</span></span>  <br/> |
|<span data-ttu-id="690ae-110">数据类型：</span><span class="sxs-lookup"><span data-stu-id="690ae-110">Data type:</span></span>  <br/> |<span data-ttu-id="690ae-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="690ae-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="690ae-112">区域：</span><span class="sxs-lookup"><span data-stu-id="690ae-112">Area:</span></span>  <br/> |<span data-ttu-id="690ae-113">传输收件人</span><span class="sxs-lookup"><span data-stu-id="690ae-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="690ae-114">备注</span><span class="sxs-lookup"><span data-stu-id="690ae-114">Remarks</span></span>

<span data-ttu-id="690ae-115">值为 TRUE 的此属性表示与会者提出建议新的日期和/或时间。</span><span class="sxs-lookup"><span data-stu-id="690ae-115">A value of TRUE for this property indicates that the attendee proposed a new date and/or time.</span></span> <span data-ttu-id="690ae-116">值为 FALSE 或不存在此属性是指与会者不具有尚未响应，或从参与者的最新响应未不包括新的日期 / 时间建议。</span><span class="sxs-lookup"><span data-stu-id="690ae-116">A value of FALSE, or the absence of this property, means either that the attendee has not yet responded, or the most recent response from the attendee did not include a new date/ time proposal.</span></span> <span data-ttu-id="690ae-117">该值必须在 TRUE 不是定期系列中的与会者。</span><span class="sxs-lookup"><span data-stu-id="690ae-117">This value must not be TRUE for attendees in a recurring series.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="690ae-118">相关资源</span><span class="sxs-lookup"><span data-stu-id="690ae-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="690ae-119">协议规范</span><span class="sxs-lookup"><span data-stu-id="690ae-119">Protocol specifications</span></span>

<span data-ttu-id="690ae-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="690ae-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="690ae-121">提供了相关的 Exchange Server 协议规范参考。</span><span class="sxs-lookup"><span data-stu-id="690ae-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="690ae-122">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="690ae-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="690ae-123">指定的属性和约会、 会议请求和响应消息的操作。</span><span class="sxs-lookup"><span data-stu-id="690ae-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="690ae-124">头文件</span><span class="sxs-lookup"><span data-stu-id="690ae-124">Header files</span></span>

<span data-ttu-id="690ae-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="690ae-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="690ae-126">提供数据类型定义。</span><span class="sxs-lookup"><span data-stu-id="690ae-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="690ae-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="690ae-127">Mapitags.h</span></span>
  
> <span data-ttu-id="690ae-128">包含作为替代名称列出的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="690ae-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="690ae-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="690ae-129">See also</span></span>



[<span data-ttu-id="690ae-130">MAPI 属性</span><span class="sxs-lookup"><span data-stu-id="690ae-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="690ae-131">MAPI 规范属性</span><span class="sxs-lookup"><span data-stu-id="690ae-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="690ae-132">映射到 MAPI 名称的规范属性名称</span><span class="sxs-lookup"><span data-stu-id="690ae-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="690ae-133">MAPI 名称映射到规范属性名称</span><span class="sxs-lookup"><span data-stu-id="690ae-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
